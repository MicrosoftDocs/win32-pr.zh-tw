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
# <a name="pfn_dxcore_notification_callback-callback"></a><span data-ttu-id="708b1-103">PFN_DXCORE_NOTIFICATION_CALLBACK 回呼</span><span class="sxs-lookup"><span data-stu-id="708b1-103">PFN_DXCORE_NOTIFICATION_CALLBACK callback</span></span>

<span data-ttu-id="708b1-104">回呼函式 (由您的應用程式所執行) ，由 DXCore 物件針對通知事件呼叫。</span><span class="sxs-lookup"><span data-stu-id="708b1-104">A callback function (implemented by your application), which is called by a DXCore object for notification events.</span></span>

## <a name="syntax"></a><span data-ttu-id="708b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="708b1-105">Syntax</span></span>

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a><span data-ttu-id="708b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="708b1-106">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="708b1-107">notificationType</span><span class="sxs-lookup"><span data-stu-id="708b1-107">notificationType</span></span>

<span data-ttu-id="708b1-108">類型： **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="708b1-108">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="708b1-109">表示此調用的通知類型。</span><span class="sxs-lookup"><span data-stu-id="708b1-109">The type of notification representing this invocation.</span></span> <span data-ttu-id="708b1-110">請參閱 [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) 中的表格，以取得哪些類型適用于哪些類型的物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="708b1-110">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about what types are valid with which kinds of objects.</span></span>

### <a name="object"></a><span data-ttu-id="708b1-111">物件 (object)</span><span class="sxs-lookup"><span data-stu-id="708b1-111">object</span></span>

<span data-ttu-id="708b1-112">類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="708b1-112">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="708b1-113">引發通知的 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="708b1-113">The [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object raising the notification.</span></span>

### <a name="context-in"></a><span data-ttu-id="708b1-114">內容 [in]</span><span class="sxs-lookup"><span data-stu-id="708b1-114">context [in]</span></span>

<span data-ttu-id="708b1-115">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="708b1-115">Type: **void\***</span></span>

<span data-ttu-id="708b1-116">指標，可能是 `nullptr` 包含內容資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="708b1-116">A pointer, which may be `nullptr`, to an object containing context info.</span></span>

## <a name="see-also"></a><span data-ttu-id="708b1-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="708b1-117">See also</span></span>

<span data-ttu-id="708b1-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="708b1-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>