---
description: WMI 提供者也可以維護記錄。 哪些記錄檔會出現在系統上，視安裝的提供者而定。
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: WMI 提供者記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9cc74b9f1c6be16f1d85eb1e1863e0dc8b7b33
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880005"
---
# <a name="wmi-provider-log-files"></a>WMI 提供者記錄檔

WMI 提供者也可以維護記錄。 哪些記錄檔會出現在系統上，視安裝的提供者而定。

這些記錄檔可能位於% systemroot% \\ system32 \\ wbem 記錄檔 \\ 目錄中。

-   [Wmiprov .log](#wmiprovlog)
-   [Ntevt .log](#ntevtlog)
-   [Dsprovider .log](#dsproviderlog)
-   [相關主題](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov .log

Wmiprov 檔案包含已啟用 WMI 的 Windows Driver Model (WDM) 驅動程式和[wdm 提供者](/windows/desktop/WmiCoreProv/wdm-provider)的管理資料和事件。 它會提供警告和錯誤資訊，主要用於疑難排解和偵測使用它的提供者和用戶端應用程式。

Wmiprov 包含：

-   來自 [WDM 提供者](/windows/desktop/WmiCoreProv/wdm-provider) 或設備磁碟機的錯誤，例如二元 MOF 編譯失敗或無法取出資料。
-   針對每個使用 MOF 格式的驅動程式，MOF 的狀態會進行編譯。
-   提供者結構和解構事件。
-   WNODE 的列印。

## <a name="ntevtlog"></a>Ntevt .log

Ntevt 檔案包含 [事件記錄提供者](/previous-versions/windows/desktop/eventlogprov/event-log-provider)的追蹤訊息。

## <a name="dsproviderlog"></a>Dsprovider .log

Dsprovider 記錄檔包含 [Active Directory 提供者](/previous-versions/windows/desktop/dsprov/active-directory-provider)的追蹤資訊和錯誤訊息。

下表列出一些可能會發生的常見問題，並提供可能的原因和解決方案。



| 訊息                                                                                                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RootDSE 上的 CLDAPClassProvider：： InitializeLDAPProvider ADsGetObject 失敗： &lt; hresult&gt;                                                                                                                                                                                                                    | 嘗試取得目錄服務的根目錄時，ADSI 呼叫失敗。 確認您的電腦是網域的成員。                                                                                                                                                                                                                                                                             |
| <class name>具有 hresult 的 CDSClassProvider：： GetObjectAsync () GETCLASSFROMCACHEORADSI &lt; 失敗&gt;                                                                                                                                                                                                  | 您嘗試取得的類別不是目錄中的有效類別。 確認類別名稱是正確的。                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider：在 LDAP：//CN = foo1，CN = Users，DC = dsprovider，DC = nttest，DC = Microsoft，DC = com with hresult 的:P utInstanceAsync () ModifyExistingInstance 失敗 &lt;&gt;                                                                                                                                       | 提供者無法將修改過的實例寫入目錄服務。 確定您使用的是 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 介面，以指定您要修改的屬性集。 如需有關如何搭配使用 **IWbemCoNtext** 介面和 [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))的詳細資訊，請參閱 [更新整個實例](updating-an-entire-instance.md)。 |
| CLDAPHelper：： GetADSIInstance ADsOpenObject () 在 hresult 上失敗 <class name> &lt;&gt;<br/> CLDAPInstanceProvider：： GetObjectAsync： GetADSIInstance () 失敗， &lt; hresult&gt;<br/> Ds 使用者的 CLDAPInstanceProvider：： GetObjectAsync () 失敗 \_ 。ADSIPath = "<class name><br/> | 這三個訊息表示您嘗試取得的實例不存在於目錄服務中。 確認 **ADSIPath** 值和類別名稱正確無誤。                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 記錄檔](wmi-log-files.md)
</dt> </dl>

 

