---
title: " (Windows 篩選平台) 的存取控制"
description: 在 Windows 篩選平台 (WFP) 中，基底篩選引擎 (BFE) 服務會根據存取權杖和安全描述項來實行標準的 Windows 存取控制模型。
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104321371"
---
# <a name="access-control-windows-filtering-platform"></a> (Windows 篩選平台) 的存取控制

在 Windows 篩選平台 (WFP) 中，基底篩選引擎 (BFE) 服務會根據存取權杖和安全描述項來實行標準的 [Windows 存取控制模型](/windows/desktop/SecAuthZ/access-control-model) 。

## <a name="access-control-model"></a>存取控制模型

加入新的 WFP 物件（例如篩選和子層）時，可以指定安全描述項。 安全描述項是使用 WFP 管理函式 **Fwpm \* GetSecurityInfo0** 和 **Fwpm \* SetSecurityInfo0** 來管理，其中 * *\** _ 代表 WFP 物件的名稱。 這些函式在語義上等同于 Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo)和 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)函數。

> [!Note]  
> 無法從明確交易中呼叫 **Fwpm \* SetSecurityInfo0** 函數。

 

> [!Note]  
> 如果 **Fwpm \* SetSecurityInfo0** 函式是用來管理在相同會話內建立的動態物件，則只能從動態會話內呼叫這些函數。

 

篩選引擎的預設安全描述項 (下圖中的根引擎物件) 如下所示。

-   將內建系統管理員群組的 **一般 \_ 所有** (GA) 存取權限授與一般。
-   授與 **一般 \_ 讀取** (GR) **一般 \_ 寫入** (GW) **一般 \_ 執行** (GX) 網路設定運算子的存取權限。
-   授與 **GRGWGX** 存取權給下列服務安全識別碼 (ssid) ： MpsSvc (Windows 防火牆) 、NapAgent (網路存取保護代理程式) 、PolicyAgent (IPsec 原則代理程式) 、RpcSs (遠端程序呼叫) 和 WdiServiceHost (診斷服務裝載) 。
-   授與 **FWPM \_ ACTRL \_ OPEN** 和 **FWPM \_ ACTRL \_ 分類** 給每個人。  (這些都是 WFP 特定的存取權限，如下表所述。 ) 

其餘預設安全描述項是透過繼承來衍生。

有一些存取檢查（例如 **Fwpm \* Add0**、 **Fwpm \* CreateEnumHandle0**、 **Fwpm \* SubscribeChanges0** 函式呼叫）無法在個別物件層級進行。 針對這些函數，每個物件類型都有容器物件。 針對標準物件類型 (例如，提供者、標注、篩選) 、現有的 **Fwpm \* GetSecurityInfo0** 和 **Fwpm \* SetSecurityInfo0** 函式已多載，因此 null **GUID** 參數可識別相關聯的容器。 針對其他物件類型 (例如，網路事件和 IPsec 安全性關聯) ，有明確的函式可用於管理容器的安全性資訊。

BFE 支援自動繼承任意的存取控制清單 (DACL) 存取控制專案 (Ace) 。 BFE 不支援) Ace (SACL 的系統存取控制清單。 物件會從其容器繼承 Ace。 容器會從篩選引擎繼承 Ace。 傳播路徑如下圖所示。

![顯示 ACE 傳播路徑的圖表，以 ' Engine ' 開頭。](images/access-control.jpg)

針對標準物件類型，BFE 會強制執行所有的一般和標準存取權限。 此外，WFP 還定義了下列特定的存取權限。



| WFP 存取權                                                                                                                        | Description                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ 新增**<br/>                                       | 將物件新增至容器所需。<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ 新增 \_ 連結**<br/>                       | 需要建立物件的關聯。 例如，若要加入參考標注的篩選準則，呼叫端必須具有標注的 [新增] \_ 連結存取權。<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 閱讀 \_ TXN**<br/>    | 開始明確讀取交易的必要。<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 寫入 \_ TXN**<br/> | 開始明確寫入交易所需。<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ 分類**<br/>                        | 需要針對使用者模式層進行分類。<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ 列舉**<br/>                                    | 列舉容器中的物件所需。 不過，列舉值只會傳回呼叫端具有 FWPM \_ ACTRL READ 存取權的物件 \_ 。<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**<br/>                                    | 開啟具有 BFE 的會話時需要此參數。<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**<br/>                                    | 讀取物件的屬性時需要。<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**<br/>                 | 讀取統計資料所需。<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ 訂閱**<br/>                     | 訂閱通知所需。 訂閱者只會收到 FWPM \_ ACTRL 讀取權限之物件的通知 \_ 。<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ 寫入**<br/>                                 | 設定引擎選項的必要參數。<br/>                                                                                                                               |



 

BFE 會略過核心模式呼叫端的所有存取檢查。

為了防止系統管理員從 BFE 鎖定自己，內建 administrators 群組的成員一律會被授與 **FWPM \_ ACTRL \_ 開啟** 給引擎物件。 因此，系統管理員可以透過下列步驟重新取得存取權。

-   啟用 **SE \_ 取得 \_ 擁有權 \_ 名稱** 許可權。
-   呼叫 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)。 呼叫會成功，因為呼叫端是內建系統管理員的成員。
-   取得引擎物件的擁有權。 這會成功，因為呼叫端具有 **SE \_ 取得 \_ 擁有權 \_ 名稱** 許可權。
-   更新 DACL。 這會成功，因為擁有者一律具有 **寫入 \_ DAC** 存取權

因為 BFE 支援它自己的自訂審核，所以不會產生一般物件存取權審核。 因此，會忽略 SACL。

## <a name="wfp-required-access-rights"></a>需要 WFP 存取權限

下表顯示 WFP 函數所需的存取權限，以便存取各種篩選平臺物件。 **FwpmFilter \* *_ 函數會列為存取標準物件的範例。所有存取標準物件的其他* 函式都會遵循 _ FwpmFilter \*** 函式存取模型。



函式

已核取物件

所需的存取

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

引擎

**FWPM \_ ACTRL \_ OPEN**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

引擎

**FWPM \_ ACTRL \_ READ**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

引擎

**FWPM \_ ACTRL \_ 寫入**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

引擎

**FWPM \_ ACTRL \_ 列舉**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

引擎

**FWPM \_ACTRL \_ BEGIN \_ READ \_ TXN**  &  **FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

容器提供者<br/> 層<br/> Sub-Layer<br/> 圖說文字<br/> 提供者內容<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ 新增 \_ 連結**<br/> **FWPM \_ ACTRL \_ 新增 \_ 連結**<br/> **FWPM \_ ACTRL \_ 新增 \_ 連結**<br/> **FWPM \_ ACTRL \_ 新增 \_ 連結**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

篩選

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

篩選

**FWPM \_ ACTRL \_ READ**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

容器篩選<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ READ**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

容器

**FWPM \_ ACTRL \_ 訂閱**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

容器

**FWPM \_ ACTRL \_ READ**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

IPsec SA 資料庫

**FWPM \_ ACTRL \_ READ \_ STATS**

[**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaCoNtextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaCoNtextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaCoNtextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

IPsec SA 資料庫

**FWPM \_ ACTRL \_ 新增**

[**IPsecSaCoNtextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaCoNtextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

IPsec SA 資料庫

**DELETE**

[**IPsecSaCoNtextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

IPsec SA 資料庫

**FWPM \_ ACTRL \_ READ**

[**IPsecSaCoNtextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

IPsec SA 資料庫

**FWPM \_ACTRL \_ 列舉**  &  **FWPM \_ ACTRL \_ READ**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

IKE SA 資料庫

**FWPM \_ ACTRL \_ READ \_ STATS**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

IKE SA 資料庫

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

IKE SA 資料庫

**FWPM \_ ACTRL \_ READ**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

IKE SA 資料庫

**FWPM \_ACTRL \_ 列舉**  &  **FWPM \_ ACTRL \_ READ**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

容器

**FWPM \_ ACTRL \_ 列舉**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

除了個別篩選和提供者內容以外，不會有其他存取權檢查



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**標準存取權限**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Windows 存取控制模型](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Windows 篩選平台存取權限識別碼**](access-right-identifiers.md)
</dt> </dl>

 

