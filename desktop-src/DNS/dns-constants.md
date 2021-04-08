---
title: DNS 常數
description: 以下是以主機位元組順序為 DNS 定義的常數。
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64497e14d6c4ae11f4a6ed68200614aa4f602270
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023098"
---
# <a name="dns-constants"></a>DNS 常數

以下是以主機位元組順序為 DNS 定義的常數。

## <a name="dns-record-types"></a>DNS 記錄類型



| 常數           | 值            |
|--------------------|------------------|
| DNS \_ 類型 \_ A       | 0x0001           |
| DNS \_ 類型 \_ NS      | 0x0002           |
| DNS \_ 類型 \_ MD      | 0x0003           |
| DNS \_ 類型 \_ MF      | 0x0004           |
| DNS \_ 類型 \_ CNAME   | 0x0005           |
| DNS \_ 類型 \_ SOA     | 0x0006           |
| DNS \_ 類型 \_ MB      | 0x0007           |
| DNS \_ 類型 \_ MG      | 0x0008           |
| DNS \_ 型別 \_ MR      | 0x0009           |
| DNS \_ 類型 \_ 為 Null    | 0x000a           |
| DNS \_ 類型 \_ WKS     | 0x000b           |
| DNS \_ 類型 \_ PTR     | 0x000c           |
| DNS \_ 類型 \_ HINFO   | 0x000d           |
| DNS \_ 類型 \_ MINFO   | 0x000e           |
| DNS \_ 類型 \_ MX      | 0x000f           |
| DNS \_ 類型 \_ 文字    | 0x0010           |
| DNS \_ 類型 \_ RP      | 0x0011           |
| DNS \_ 類型 \_ AFSDB   | 0x0012           |
| DNS \_ 類型 \_ X25     | 0x0013           |
| DNS \_ 類型 \_ ISDN    | 0x0014           |
| DNS \_ 類型 \_ RT      | 0x0015           |
| DNS \_ 類型的 \_ NSAP    | 0x0016           |
| DNS \_ 類型 \_ NSAPPTR | 0x0017           |
| DNS \_ 類型的 \_ SIG     | 0x0018           |
| DNS \_ 類型 \_ 金鑰     | 0x0019           |
| DNS \_ 類型 \_ PX      | 0x001a           |
| DNS \_ 類型 \_ GPO    | 0x001b           |
| DNS \_ 類型 \_ AAAA    | 0x001c           |
| DNS \_ 類型 \_ LOC     | 0x001d           |
| DNS \_ 類型 \_ NXT     | 0x001e           |
| DNS \_ 類型的 \_ EID     | 0x001f           |
| DNS \_ 類型 \_ NIMLOC  | 0x0020           |
| DNS \_ 類型 \_ SRV     | 0x0021           |
| DNS \_ 類型 \_ ATMA    | 0x0022           |
| DNS \_ 類型 \_ NAPTR   | 0x0023           |
| DNS \_ 類型 \_ KX      | 0x0024           |
| DNS \_ 類型 \_ CERT    | 0x0025           |
| DNS \_ 類型 \_ A6      | 0x0026           |
| DNS \_ 類型 \_ DNAME   | 0x0027           |
| DNS \_ 類型 \_ 接收    | 0x0028           |
| DNS \_ 類型 \_ OPT     | 0x0029           |
| DNS \_ 類型 \_ DS      | 0x002B           |
| DNS \_ 類型 \_ RRSIG   | 0x002E           |
| DNS \_ 類型 \_ NSEC    | 0x002F           |
| DNS \_ 類型的 \_ DNSKEY  | 0x0030           |
| DNS \_ 類型 \_ DHCID   | 0x0031           |
| DNS \_ 類型 \_ UINFO   | 0x0064           |
| DNS \_ 類型 \_ UID     | 0x0065           |
| DNS \_ 類型 \_ GID     | 0x0066           |
| DNS \_ 類型 \_ UNSPEC  | 0x0067           |
| DNS \_ 類型 \_ ADDRS   | 0x00f8           |
| DNS \_ 類型 \_ TKEY    | 0x00f9           |
| DNS \_ 類型 \_ TSIG    | 0x00fa           |
| DNS \_ 類型的 \_ IXFR    | 0x00fb           |
| DNS \_ 類型 \_ AXFR    | 0x00fc           |
| DNS \_ 類型 \_ MAILB   | 0x00fd           |
| DNS \_ 類型 \_ MAILA   | 0x00fe           |
| DNS \_ 類型 \_ 全部     | 0x00ff           |
| DNS \_ 類型 \_     | 0x00ff           |
| DNS \_ 類型 \_ 獲勝    | 0xff01           |
| DNS \_ 類型 \_ WINSR   | 0xff02           |
| DNS \_ 類型 \_ NBSTAT  | DNS \_ 類型 \_ WINSR |



 

## <a name="dns-class-types"></a>DNS 類別類型



| 常數             | 值  |
|----------------------|--------|
| DNS \_ 類別 \_ 網際網路 | 0x0001 |
| DNS \_ 類別 \_ CSNET    | 0x0002 |
| DNS \_ 類別 \_ 混亂    | 0x0003 |
| DNS \_ 類別 \_ HESIOD   | 0x0004 |
| DNS \_ 類別 \_ 無     | 0x00fe |
| DNS \_ 類別 \_ 全部      | 0x00ff |
| DNS \_ 類別 \_ ANY      | 0x00ff |



 

## <a name="dns-query-types"></a>DNS 查詢類型



| 常數                    | 值  |
|-----------------------------|--------|
| DNS \_ OPCODE \_ 查詢          | 0x0000 |
| DNS \_ OPCODE \_ IQUERY         | 0x0001 |
| DNS \_ OPCODE \_ 伺服器 \_ 狀態 | 0x0002 |
| DNS \_ OPCODE \_ 不明        | 0x0003 |
| DNS \_ 操作碼 \_ 通知         | 0x0004 |
| DNS \_ 操作碼 \_ 更新         | 0x0005 |



 

## <a name="dns-record-flags"></a>DNS 記錄旗標

下列旗標會參考 DNS 訊息中資源記錄的 (RR) 區段：



| 常數           | 值      | 意義                         |
|--------------------|------------|---------------------------------|
| DNSREC \_ 問題   | 0x00000000 | RR 在問題區段中   |
| DNSREC \_ 解答     | 0x00000001 | RR 位於答案區段     |
| DNSREC \_ 授權單位  | 0x00000002 | RR 位於授權單位區段  |
| DNSREC \_ 其他 | 0x00000003 | RR 位於其他區段 |



 

下列旗標會參考每個 [RFC 2136](https://www.ietf.org/rfc/rfc2136.txt)的 update DNS 訊息內的 RR 區段：



| 常數       | 值      | 意義                           |
|----------------|------------|-----------------------------------|
| DNSREC \_ 區域   | 0x00000000 | RR 在區域區段中         |
| DNSREC \_ >PREREQ | 0x00000001 | RR 位於先決條件區段 |
| DNSREC \_ 更新 | 0x00000002 | RR 在 update 區段中       |



 

下列旗標互斥：



| 常數        | 值      | 意義                                                    |
|-----------------|------------|------------------------------------------------------------|
| DNSREC \_ 刪除  | 0x00000004 | 刪除 RR。 搭配 DNSREC \_ 更新使用       |
| DNSREC \_ NOEXIST | 0x00000004 | RR 不存在。 搭配 DNSREC \_ >prereq 使用 |



 

## <a name="dns-query-options"></a>DNS 查詢選項



| 常數                                | 值      | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DNS \_ 查詢 \_ 標準                    | 0x00000000 | 標準查詢。                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DNS \_ 查詢 \_ 接受 \_ 截斷的 \_ 回應 | 0x00000001 | 傳回截斷的結果。 不會在 TCP 下重試。                                                                                                                                                                                                                                                                                                                                                                                                   |
| DNS \_ 查詢 \_ \_ 僅使用 TCP \_              | 0x00000002 | 只針對查詢使用 TCP。                                                                                                                                                                                                                                                                                                                                                                                                                           |
| DNS \_ 查詢 \_ 沒有 \_ 遞迴               | 0x00000004 | 指示 DNS 伺服器執行反復查詢 (特別指示 DNS 伺服器不執行遞迴解析來解析查詢) 。                                                                                                                                                                                                                                                                                                   |
| DNS \_ 查詢 \_ 略過快取 \_               | 0x00000008 | 略過查閱上的 [*解析程式*](r-gly.md) 快取。                                                                                                                                                                                                                                                                                                                                                                            |
| DNS \_ 查詢 \_ 沒有 \_ 線路 \_ 查詢             | 0x00000010 | 指示 DNS 只在本機快取上執行查詢。**Windows 2000 Server 和 windows 2000 Professional：** 不支援這個值。 如需類似的功能，請 **\_ \_ \_ 只使用 DNS 查詢** 快取。<br/>                                                                                                                                                                                                                                      |
| DNS \_ 查詢 \_ 沒有 \_ 本機 \_ 名稱             | 0x00000020 | 指示 DNS 忽略本機名稱。**Windows 2000 Server 和 windows 2000 Professional：** 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                                    |
| DNS \_ 查詢 \_ 沒有 \_ 主機 \_ 檔案             | 0x00000040 | 防止 DNS 查詢查閱主機檔案。**Windows 2000 Server 和 windows 2000 Professional：** 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                   |
| DNS \_ 查詢 \_ 沒有 \_ NETBT                   | 0x00000080 | 防止 DNS 查詢使用 NetBT 來解決問題。**Windows 2000 Server 和 windows 2000 Professional：** 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ 僅限 DNS 查詢網路 \_                  | 0x00000100 | 指示 DNS 只使用網路執行查詢，略過本機資訊。**Windows 2000 Server 和 windows 2000 Professional：** 不支援這個值。<br/>                                                                                                                                                                                                                                                                      |
| DNS \_ 查詢 \_ 傳回 \_ 訊息             | 0x00000200 | 指示 DNS 傳回整個 DNS 回應訊息。**Windows 2000 Server 和 windows 2000 Professional：** 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                   |
| \_僅 DNS 查詢 \_ 多播 \_             | 0x00000400 | 防止查詢使用 DNS，並且只使用本機連結多播名稱解析 (LLMNR) 。**Windows Vista 和 Windows Server 2008 或更新版本。：** 這是支援的值。<br/>                                                                                                                                                                                                                                                                  |
| DNS \_ 查詢 \_ 沒有 \_ 多播               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DNS \_ 查詢 \_ 視為 \_ \_ FQDN             | 0x00001000 | 防止 DNS 回應將尾碼附加至名稱解析程式中提交的名稱。                                                                                                                                                                                                                                                                                                                                                  |
| DNS \_ 查詢 \_ ADDRCONFIG                  | 0x00002000 | 僅限 Windows 7：如果沒有可用的 IPv4 位址，請不要 [**傳送型別**](/windows/win32/api/windns/ns-windns-dns_a_data) 查詢，如果 IPv6 位址無法使用，則不傳送 [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) 型別查詢。                                                                                                                                                                                                                                   |
| DNS \_ 查詢 \_ 雙重 \_ 位址                  | 0x00004000 | 僅限 Windows 7：查詢 [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) 和 [**類型記錄**](/windows/win32/api/windns/ns-windns-dns_a_data) ，並傳回每個的結果。 **類型記錄的結果** 會對應至 **AAAA** 類型。                                                                                                                                                                                                                                                           |
| DNS \_ 查詢 \_ 多播 \_ 等候             | 0x00020000 | 等候完整的超時時間，以收集來自本機連結的所有回應。 如果未設定，則預設行為會傳回第一個回應。**Windows Vista 和 Windows Server 2008 或更新版本。：** 這是支援的值。<br/>                                                                                                                                                                                                              |
| DNS \_ 查詢 \_ 多播 \_ 驗證           | 0x00040000 | 使用本機電腦主機名稱來指示測試，以驗證相同本機連結的名稱唯一性。 收集所有回應，即使未啟用一般 LLMNR 傳送者行為也是一樣。**Windows Vista 和 Windows Server 2008 或更新版本。：** 這是支援的值。<br/>                                                                                                                                                                                  |
| DNS \_ 查詢不會 \_ \_ 重設 \_ TTL \_ 值    | 0x00100000 | 如果設定，且回應包含多筆記錄，則記錄會與所有記錄中最小值 TTL 對應的 TTL 一併儲存。 當設定此選項時，不會修改傳回記錄集中的「不要變更個別記錄的 TTL」。                                                                                                                                                                               |
| DNS \_ 查詢 \_ 停用 \_ IDN \_ 編碼      | 0x00200000 | 停用 [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a)、 [**DnsQueryEx**](/windows/desktop/api/Windns/nf-windns-dnsqueryex)、 [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)和 [**DNSREPLACERECORDSET**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) api 中的國際功能變數名稱 (IDN) 編碼支援。 所有的 punycode 名稱都會被視為 ASCII，而且會在網路上以 ASCII 編碼。 所有非 ASCII 名稱都會在網路上以 UTF8 編碼。 **Windows 8 或更新版本。：** 這是支援的值。<br/> |
| DNS \_ 查詢 \_ 附加 \_ 多標籤          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DNS \_ 查詢 \_ 保留                    | 0xf0000000 | 保留的。                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>DNS 更新選項



| 常數                                 | 值      | 意義                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DNS \_ 更新 \_ 安全性 \_ 使用 \_ 預設值      | 0x00000000 | 使用登錄中指定的預設行為，以進行安全的動態 DNS 更新。                                                                |
| DNS \_ 更新 \_ 安全性 \_ 關閉               | 0x00000010 | 不會嘗試安全的動態更新。                                                                                                                      |
| \_ \_ 上的 DNS 更新安全性 \_                | 0x00000020 | 嘗試不安全的動態更新;如果拒絕，則會嘗試安全動態更新。                                                                               |
| \_ \_ 僅限 DNS 更新安全性 \_              | 0x00000100 | 只會嘗試保護動態更新。                                                                                                                         |
| DNS \_ 更新快取 \_ \_ 安全性 \_ 內容    | 0x00000200 | 快取安全性內容以用於未來的交易。                                                                                                   |
| DNS \_ 更新 \_ 測試 \_ 使用 \_ 本機 \_ SYS \_ 帳戶 | 0x00000400 | 使用本機電腦帳戶的認證。                                                                                                               |
| DNS \_ 更新 \_ 強制 \_ 安全性 \_ NEGO       | 0x00000800 | 不會使用快取的安全性內容。                                                                                                                         |
| DNS \_ 更新 \_ 嘗試 \_ 所有 \_ 主 \_ 伺服器   | 0x00001000 | 將 DNS 更新傳送至所有多宿主 DNS 伺服器。                                                                                                            |
| DNS \_ 更新 \_ 略過 \_ 沒有 \_ 更新 \_ 介面卡  | 0x00002000 | 請勿更新已停用動態 DNS 更新的介面卡。**Windows 2000 SERVER SP2 或更新版本。：** 這是支援的值。<br/>                 |
| DNS \_ 更新 \_ 遠端 \_ 伺服器              | 0x00004000 | 除了本機 DNS 伺服器之外，在遠端伺服器上註冊 CNAME 記錄。**Windows 2000 SERVER SP2 或更新版本。：** 這是支援的值。<br/> |
| DNS \_ 更新 \_ 保留                    | 0xffff0000 | 保留供未來使用。                                                                                                                                      |



 

## <a name="dns-response-codes"></a>DNS 回應碼



| 錯誤                | 意義                                        |
|----------------------|------------------------------------------------|
| DNS \_ RCODE \_ >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR  | 沒有錯誤                                       |
| DNS \_ RCODE \_ FORMERR  | 格式錯誤                                   |
| DNS \_ RCODE \_ SERVFAIL | 伺服器失敗                                 |
| DNS \_ RCODE \_ NXDOMAIN | 名稱錯誤                                     |
| DNS \_ RCODE \_ >NOTIMPL  | 未實作                                |
| \_拒絕 DNS RCODE \_  | 連線被拒                             |
| DNS \_ RCODE \_ YXDOMAIN | 功能變數名稱不應存在                   |
| DNS \_ RCODE \_ YXRRSET  | 資源記錄 (RR) 集不應存在      |
| DNS \_ RCODE \_ NXRRSET  | RR 集不存在                          |
| DNS \_ RCODE \_ NOTAUTH  | 未授權區域                     |
| DNS \_ RCODE \_ NOTZONE  | 名稱不在區域中                               |
| DNS \_ RCODE \_ BADVERS  | 適用于 DNS (EDNS) 版本的擴充機制不正確 |
| DNS \_ RCODE \_ BADSIG   | 錯誤的簽章                                  |
| DNS \_ RCODE \_ BADKEY   | 錯誤的索引鍵                                        |
| DNS \_ RCODE \_ BADTIME  | 錯誤的時間戳記                                  |



 

 

 





