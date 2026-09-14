# IPCheckRule

IP 检测与泄漏检测站点规则清单，提供可直接用于规则集的多种格式文件。

## 文件说明

- `ip-check.list`：域名规则源列表（`+.domain`）。
- `ip-check.yaml`：YAML `payload` 格式规则，可直接引用。
- `ip-check.mrs`：预构建二进制规则文件。

## 规则范围

当前收录 **68** 个与以下场景相关的站点域名：

- IP 查询
- 归属地 / Geo / ASN 数据库与 API
- 纯净度 / 黑名单 / 风险评分
- DNS / WebRTC / IPv6 泄漏检测

## 使用方式

按你的规则引擎需要选择文件：

- 需要纯文本域名列表时使用 `ip-check.list`
- 需要 `payload` YAML 规则时使用 `ip-check.yaml`
- 支持二进制规则集时使用 `ip-check.mrs`

## 维护原则

- 使用 `domain` 行为（`+.domain`）维护源列表。
- `ip-check.list` 与 `ip-check.yaml` 必须保持条目一致、顺序一致。
- `ip-check.mrs` 由 `ip-check.yaml` 自动生成并保持同步。