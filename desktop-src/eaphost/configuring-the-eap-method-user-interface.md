---
title: 設定 EAP 方法消費者介面
description: 說明如何將 EAP 方法設定提供給 EAPHost，以設定要求者。
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6709e68bf20d8f38d3685f66e45313083e70e46b1a8a0bb0675616bdb4e8bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086702"
---
# <a name="configuring-the-eap-method-user-interface"></a>設定 EAP 方法消費者介面

本主題說明如何將 EAP 方法設定提供給 EAPHost，以設定要求者。

若要讓要求者使用 EAPHost 執行 EAP 型驗證，要求者必須透過 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 函式將 eap 方法設定提供給 EAPHost。

1.  為了取得 EAP 方法設定，要求者通常會使用 [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) 查詢 EAPHost，以瞭解在本機電腦上可用且已安裝的一組完整 EAP 方法。 方法清單通常會在下拉式列示方塊或其他 UI 控制項中呈現給使用者，讓使用者選取他們想要的方法。
    > [!Note]  
    > 要求者可以根據 **EAP \_ 方法 \_ 資訊 eapProperties** 中指出的方法屬性位，選擇篩選顯示的方法清單。 例如，某些方法可能不適合要求者所提供之傳輸的安全性特性。

     

2.  當 UI 控制項填入一組可能的 EAP 方法之後，使用者會選取想要設定的方法。 通常，要求者會提供 [設定 **] 或 [** **屬性** ] 按鈕，讓使用者存取所選 EAP 方法的設定屬性。
    > [!Note]
    > 要求者知道有使用者可設定的屬性是以 **EAP \_ 方法 \_ 資訊 eapProperties** 中啟用的 **eapPropSupportsConfig** 位為基礎。
    >
    > 如需詳細資訊，請參閱 [**EAP 方法屬性**](eap-method-properties.md)。

     

3.  當使用者按一下適當的 UI 控制項時，要求者會呼叫 [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)，並將要求者本身 UI 的 **HWND** 值、從查詢取得的 [**eap \_ 方法 \_ 類型**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) 結構，以及其他必要的參數 [**傳遞至函式 \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) 。
4.  呼叫 [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) 會叫用 EAP 方法本身的設定 UI。 從 **EapHostPeerInvokeConfigUI** 傳回時，函式會傳回 EAP 方法設定 BLOB 做為 out 參數。
5.  要求者會儲存設定 BLOB，以及搭配 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)使用的 [**EAP \_ 方法 \_ 類型**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)結構。
6.  儲存組態 BLOB 的精確方法完全取決於要求者。 不過，要求者應該一律以適當且安全的方式儲存設定，以適合系統和使用者驗證設定資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟用群組原則](enabling-group-policy.md)
</dt> <dt>

[為 EAP 方法執行 In-Band NAP 支援](enabling-in-band-nap-support.md)
</dt> <dt>

[為 EAP 方法執行 NAP 支援](implementing-nap-for-eap-methods.md)
</dt> <dt>

[在要求者和 EAP 方法之間傳送資料](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost 要求者](eaphost-supplicants.md)
</dt> </dl>

 

 




