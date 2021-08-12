---
title: 為 EAP 方法執行 NAP 支援
description: 瞭解如何為 EAPHost 要求者實行 NAP 支援。 請參閱 EAPHost 相關的 NAP 主題，並查看其他可用的資源。
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff84c24aeb475b83146f2c56e9e139fd930eac27656349c594f05d91c1036fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273312"
---
# <a name="implementing-nap-support-for-eap-methods"></a>為 EAP 方法執行 NAP 支援

本主題說明如何為 EAPHost 要求者執行 NAP。 在 Windows Vista 和 Windows Server 2008 中，NAP 強制用戶端 (NAP EC) 適用于[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10))驗證連接。

## <a name="implementing-network-access-protection-nap"></a> (NAP) 執行網路存取保護

為了支援 NAP，EAPHost 要求者會執行符合 [**NotificationHandler**](/previous-versions/windows/desktop/api) 回呼原型的回呼函式，而且必須在呼叫 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)時提供此回呼函數的指標。

回呼函式會採用兩個參數。

-   GUID，可唯一識別與驗證相關聯的介面。
-   要求者所提供之不透明資料結構的 VOID 指標。

當機器的隔離狀態變更時，EAPHost 會呼叫要求者提供的回呼函式，並搭配唯一的介面 GUID 和 VOID 指標。 當 EAPHost 呼叫要求者提供的回呼函式時，要求者會藉由卸載 interface GUID/VOID 指標所識別的邏輯網路連線，並使用 **EapHostPeerBeginSession** 再次開始驗證，來回應。

EAPHost 可能會在任何時間呼叫要求者提供的回呼函式：在主動驗證期間，或在完成驗證之後 (在呼叫 [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) 之後，但在呼叫 [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) 之前未呼叫過，) 。 要求者應該一律透過卸載邏輯網路連線並重新驗證，來回應。

如果要求者正在關閉或選擇不再收到隔離狀態變更的通知，要求者應該呼叫 [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) 並指定適當的介面 GUID。 如果要求者想要判斷邏輯網路連接的隔離，要求者可以從 [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)取得 [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)時，從 **EapHostPeerMethodResult** 取得該資訊。

## <a name="eaphost-related-nap-information"></a>EAPHost 相關的 NAP 資訊

如需 EAPHost API 相關 NAP 資訊，請參閱下列主題。

-   [**EAP \_ 屬性 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**EAP \_ 錯誤**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [EAPHost 要求者的常見問題](eaphost-supplicant-frequently-asked-questions.md)
-   [**EAP 方法屬性**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**EAP 相關的錯誤和資訊常數**](eap-related-error-and-information-constants.md)
-   [**隔離 \_ 狀態**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>其他資源


-   如需 NAP 資源的清單，請參閱 [網路存取保護](https://go.microsoft.com/fwlink/p/?linkid=84107)。
-   如需健康狀態資訊的聲明，請參閱「 [網路存取保護」 (NAP) 健康狀態聲明 (SoH) 訊息](https://go.microsoft.com/fwlink/p/?linkid=83918)。
-   如需 Enterprise 網路群組網頁和 blog，請參閱[網路存取保護 (NAP) ](https://go.microsoft.com/fwlink/p/?linkid=83845)。
-   如需 NAP API 資訊，請參閱 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page)。


## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 EAP 方法消費者介面](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[啟用群組原則](enabling-group-policy.md)
</dt> <dt>

[為 EAP 方法執行 In-Band NAP 支援](enabling-in-band-nap-support.md)
</dt> <dt>

[在要求者和 EAP 方法之間傳送資料](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost 要求者](eaphost-supplicants.md)
</dt> </dl>

 

 