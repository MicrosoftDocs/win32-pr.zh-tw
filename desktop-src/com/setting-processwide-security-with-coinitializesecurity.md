---
title: 使用 CoInitializeSecurity 設定 Process-Wide 安全性
description: CoInitializeSecurity 函式可讓您以程式設計方式設定應用程式的安全性，以控制複雜的安全性案例。
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567a6dfaf47dbd278fc248558cd25969c733b24a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382982"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>使用 CoInitializeSecurity 設定 Process-Wide 安全性

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)函式可讓您以程式設計方式設定應用程式的安全性，以控制複雜的安全性案例。 本主題說明您可能使用 **CoInitializeSecurity** 的案例，並提供其使用方式的一些詳細資料。

有幾個原因會導致您可能想要使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 在程式內設定整個進程的安全性。 例如，雖然您可以使用 dcomcnfg.exe 來設定應用程式的驗證層級和存取權限，但電腦的預設模擬等級可能不是您想要用於處理的電腦。 為您的程式變更這個設定的唯一方法就是呼叫 **CoInitializeSecurity**。

如果您想要使用安全通道安全性提供者，您必須在呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，將它指定為驗證服務。

您可以用程式設計方式設定整個進程安全性的另一個常見案例，就是當您想要設定整個進程的預設安全性，但是在該進程內有一個或多個物件會公開具有特殊安全性需求的介面。 在這種情況下，您可以呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定處理常式的安全性，讓 COM 能夠處理大部分的安全性檢查，您也可以呼叫其他方法來設定具有特殊安全性需求之物件的安全性。 在 [介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)時，會說明如何呼叫這些方法和函式。

如果您的應用程式具有非常特製化的安全性需求，例如允許某些群組根據一天的時間存取不同的物件，您可能會想要以程式設計方式處理所有的安全性，以確保 COM 完全不會自動檢查您的所有安全性。 若要這樣做，您必須呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)，將 *dwAuthnLevel* 參數設定為 None，並將 *pVoid* 參數設定為 **Null**。 如果您有自己的安全性封裝，您也必須在 *pAuthnSvc* 參數中註冊它。 然後，您可以透過呼叫 proxy 層級介面，以及在 [介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)所述的函式，以程式設計方式處理您的所有安全性。

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 提供一組豐富的功能。 如果您呼叫 **CoInitializeSecurity**，則會忽略登錄值，而是改用您撥入電話的安全性初始化值。 根據您想要的結果，第一個參數 *pVoid* 可指向三種不同類型的值： [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 、 [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) 物件或 AppID 的指標。 在大多數情況下，您將使用 Windows 函數來建立 *pVoid* 將指向的 **安全 \_ 描述項**。

不過， *pVoid* 也可以指向 [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) 物件。

若要 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 您要將 [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) 物件傳遞至 *PVOID*，您必須將 EOAC \_ 存取控制值傳遞給 \_ *dwCapabilities* 參數。 由於 **CoInitializeSecurity** 會快取存取檢查的結果，因此在呼叫 **CoInitializeSecurity** 之後，就不得變更存取控制清單。

另一種可傳遞給 *pVoid* 參數的值是 GUID 的指標，也就是您應用程式的 AppID。 如果 *pVoid* 是 AppID 的指標，您必須 \_ 在 *PCAPABILITIES* 參數中指定 EOAC AppID，讓函數知道 *pVoid* 中預期的值。 如果 *pVoid* 指向 AppID， [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 只會使用登錄來進行驗證值，並忽略所有其他參數來 **CoInitializeSecurity**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 Process-Wide 安全性](setting-processwide-security.md)
</dt> </dl>

 

 