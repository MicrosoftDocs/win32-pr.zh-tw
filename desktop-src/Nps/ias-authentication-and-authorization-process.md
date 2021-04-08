---
title: 叫用擴充 Dll
description: 會針對它從網路存取伺服器接收的每個有效驗證或帳戶處理封包， (NAS) 來呼叫這些函式。
ms.assetid: 6d738ad7-cce5-4835-97d6-c57173c79a16
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc96fab078a982f23f5f5dd86d51dbed46d5541
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933468"
---
# <a name="invoking-the-extension-dlls"></a>叫用擴充 Dll

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

NPS 擴充 Dll 必須匯出至少下列其中一個回呼函數： [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process)、 [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)或 [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)。 NPS 會針對它從網路存取伺服器接收的每個有效驗證或帳戶處理封包， (NAS) 來呼叫這些函式。 NPS 會在 NPS 的 Parameters 登錄機 [碼](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)底下列出的每個 dll 中呼叫這些函式。 Dll 會依列出的順序來呼叫。

如果 NPS 延伸模組 DLL 匯出上述多個函式，NPS 只會叫用其中一個函式：作業系統所支援的最新功能。

> [!Note]  
> IAS 原本僅支援 [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process)。 IAS 也支援 [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)。 IAS (和更新版本的 NPS) 也支援 [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)。

 

NPS 擴充 Dll 也可以匯出 [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) 和 [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) 函數。 如果有的話，NPS 會在服務啟動和停止時分別呼叫這些函式。

## <a name="radiusextensionprocess-callback-function"></a>RadiusExtensionProcess 回呼函式

在驗證延伸模組 DLL 中， [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) 會接收 NPS 在驗證或帳戶處理要求中收到的所有屬性。 使用這些屬性，函式可以執行額外的驗證、驗證使用者的授權，或將帳戶處理記錄傳送至中央狀態伺服器。

在授權延伸 DLL 中， **RadiusExtensionProcess** 會接收 NPS 授權服務所產生的所有屬性。 這些是 Access-Accept 封包中傳回的屬性。

在呼叫 **RadiusExtensionProcess** 之後，NPS 所執行的動作取決於 **RadiusExtensionProcess** 的傳回值，以及 *pfAction* 參數中所傳回的值。 這些值會列在下表中。



| *pfAction* | 驗證延伸模組 DLL                                                                                                                                            | 授權延伸模組 DLL                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 接受     | 略過任何進一步的驗證延伸模組 Dll，也略過 NPS 驗證機制。                                                                  | 不允許接受。                                                                                                                                         |
| 拒絕     | 略過任何進一步的驗證延伸模組 Dll，也略過 NPS 驗證機制。 傳送 Access-Reject 封包。                                    | 略過任何進一步的授權延伸模組 Dll。                                                                                                          |
| 繼續   | 如果登錄中沒有列出其他驗證延伸模組 Dll，封包會傳送至下一個驗證延伸模組 DLL 或 NPS 驗證機制。 | 如果登錄中沒有列出其他授權延伸模組 Dll，封包會傳送至下一個授權延伸模組 DLL 或 NPS 帳戶處理記錄檔。 |



 

針對所有延伸模組 Dll，如果 **RadiusExtensionProcess** 傳回錯誤，則會捨棄封包。 NPS 帳戶處理記錄檔不會處理因為錯誤而捨棄的封包。

如果發生錯誤，NPS 會將一般錯誤事件張貼至事件記錄檔。 建議延伸模組 DLL 提供其他錯誤記錄。

如需詳細資訊和代表上述進程的圖表，請參閱 [關於 NPS 擴充](/windows/desktop/Nps/ias-about-internet-authentication-service)功能。

如果 **RadiusExtensionProcess** 無法驗證封包的接受或拒絕，則應該會傳回錯誤。 如果網路問題導致 **RadiusExtensionProcess** 無法與使用者驗證資料庫通訊，就可能發生這種情況。

處理會計封包時， *pfAction* 參數為 **Null**，因此無法設定 *pfAction* 。 在處理會計要求時從 **RadiusExtensionProcess** 函式傳回錯誤，會導致 NPS 捨棄要求。

> [!Note]  
> 接收到接受之後，NPS 不會在序列的其餘 Dll 中呼叫 **RadiusExtensionProcess** 。 因為某些驗證函式也可能會執行授權，所以略過這類驗證函式可能會導致授權被省略。 如果 [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) 的實例傳回 Accept，請務必不要對所抓取的授權提出任何假設。

 

如果傳回 Continue 或 Accept，則會將對應至領域的設定檔傳回 Access-Accept 封包中。

驗證延伸模組 Dll 應設計成與內建的 NPS 驗證提供者和其他擴充 Dll 並存。 如果延伸模組只適用于特定的使用者資料庫 (例如 Windows Active Directory) ，則在處理要求之前，它應該先驗證 *pAttrs* 參數中所傳遞的 [**ratProvider**](/windows/desktop/api/authif/ne-authif-radius_authentication_provider)屬性。 RatProvider 屬性會是 *pAttrs* 參數所指向的其中一個屬性清單。

擴充 Dll 不應拒絕要求，因為遺漏必要的屬性。 例如，如果驗證延伸模組需要 User-Password 屬性、ratUserPassword，而且該屬性不存在，則此延伸模組應該會傳回 raContinue 的動作，讓其他延伸模組和提供者有機會處理要求。

NPS 會在決定使用特定的驗證資料庫之後，但在使用者進行驗證之前，呼叫 [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) 函式。 因此，此函式會提供要使用之驗證資料庫的相關資訊，讓函數可以檢查適當驗證資料庫中的使用者授權。 NPS 支援各種驗證資料庫，包括 Windows Active Directory。

## <a name="radiusextensionprocessex-callback-function"></a>RadiusExtensionProcessEx 回呼函式

NPS 擴充 Dll 可能會匯出 [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) ，而不是、或除了 [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)以外。 此函式可讓 DLL 將額外的授權屬性附加至驗證回應。

*RadiusExtensionProcess 回檔* 函式區段中所述的相同資訊適用于 [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)函數。

[**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) 無法修改或移除任何存在的屬性。 如果發生 DLL 必須修改或移除屬性的情況，唯一的選項是使用 NPS 使用者介面來確保屬性不存在。 依預設，不會有任何授權屬性。 任何存在的都必須透過使用者介面加入。

如果設定了多個授權 Dll，且其中一些 Dll 會執行 [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)，則指定 DLL 中的 **RadiusExtensionProcess/Ex** 函式不會接收先前所呼叫之授權 dll 中的屬性。 它只會接收 NPS 授權服務所產生的屬性。

## <a name="radiusextensionprocess2-callback-function"></a>RadiusExtensionProcess2 回呼函式

NPS 擴充 Dll 也可以匯出 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) ，而不是、或除了 [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) 和 **RadiusExtensionProcessEx**。 此函式可讓 DLL 在驗證要求或回應中加入、修改和移除屬性。

*RadiusExtensionProcessEx 回檔* 函式區段中所述的相同資訊適用于 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)函式，但有下列例外狀況：

-   在授權 DLL 中， **RadiusExtensionProcess2** 會接收 NPS 授權服務所產生的屬性，以及先前稱為授權 dll 產生的屬性。
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) 沒有 *pfAction* 參數。 **RadiusExtensionProcess2** 會使用 [**RADIUS \_ 延伸 \_ \_ 模組控制區塊**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)結構中提供的 [**SetResponseType**](/previous-versions/ms688462(v=vs.85))函式，來設定要求的最終處置。
-   NPS 一律會呼叫任何其餘 Dll 中的 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) 函式，而不管先前 dll 中的函式是否傳回 Accept。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定延伸模組 Dll](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[使用者識別屬性](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 