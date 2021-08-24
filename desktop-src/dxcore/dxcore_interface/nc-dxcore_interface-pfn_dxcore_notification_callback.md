---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: 回呼函式 (由您的應用程式所執行) ，由 DXCore 物件針對通知事件呼叫。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f86bef2d2183562b322cdc0b01ffb64d25b23bb64dd8967e09e2dd761f7654b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787098"
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

### <a name="object"></a>object

類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

引發通知的 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件。

### <a name="context-in"></a>內容 [in]

類型： **void \***

指標，可能是 `nullptr` 包含內容資訊的物件。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)