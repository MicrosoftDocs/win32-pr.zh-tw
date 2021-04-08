---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: 回呼函式 (由您的應用程式所執行) ，由 DXCore 物件針對通知事件呼叫。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933491"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>PFN_DXCORE_NOTIFICATION_CALLBACK 回呼

回呼函式 (由您的應用程式所執行) ，由 DXCore 物件針對通知事件呼叫。

## <a name="syntax"></a>語法

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>參數

### <a name="notificationtype"></a>notificationType

類型： **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

表示此調用的通知類型。 請參閱 [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) 中的表格，以取得哪些類型適用于哪些類型的物件的相關資訊。

### <a name="object"></a>物件 (object)

類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

引發通知的 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件。

### <a name="context-in"></a>內容 [in]

類型： **void \***

指標，可能是 `nullptr` 包含內容資訊的物件。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)