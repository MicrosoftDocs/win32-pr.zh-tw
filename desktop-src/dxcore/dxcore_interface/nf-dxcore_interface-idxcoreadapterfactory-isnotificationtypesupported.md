---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: 判斷作業系統 (OS) 是否支援指定的通知類型。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315967"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a><span data-ttu-id="3e3f1-103">IDXCoreAdapterFactory：： IsNotificationTypeSupported 方法</span><span class="sxs-lookup"><span data-stu-id="3e3f1-103">IDXCoreAdapterFactory::IsNotificationTypeSupported method</span></span>

<span data-ttu-id="3e3f1-104">判斷作業系統 (OS) 是否支援指定的通知類型。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-104">Determines whether a specified notification type is supported by the operating system (OS).</span></span> <span data-ttu-id="3e3f1-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3f1-106">語法</span><span class="sxs-lookup"><span data-stu-id="3e3f1-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a><span data-ttu-id="3e3f1-107">參數</span><span class="sxs-lookup"><span data-stu-id="3e3f1-107">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="3e3f1-108">notificationType</span><span class="sxs-lookup"><span data-stu-id="3e3f1-108">notificationType</span></span>

<span data-ttu-id="3e3f1-109">類型： **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="3e3f1-109">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="3e3f1-110">您要查詢有關支援的通知類型。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-110">The type of notification that you're querying about support for.</span></span> <span data-ttu-id="3e3f1-111">如需通知類型的相關資訊，請參閱 [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-111">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about the notification types.</span></span>

## <a name="returns"></a><span data-ttu-id="3e3f1-112">傳回</span><span class="sxs-lookup"><span data-stu-id="3e3f1-112">Returns</span></span>

<span data-ttu-id="3e3f1-113">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="3e3f1-113">Type: **bool**</span></span>

<span data-ttu-id="3e3f1-114"> `true`   如果系統支援通知型別，則會傳回。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-114">Returns `true` if the notification type is supported by the system.</span></span> <span data-ttu-id="3e3f1-115">否則，會傳回  `false` 。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-115">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e3f1-116">備註</span><span class="sxs-lookup"><span data-stu-id="3e3f1-116">Remarks</span></span>

<span data-ttu-id="3e3f1-117">您可以呼叫 **IsNotificationTypeSupported** ，判斷這個作業系統版本是否知道指定的通知類型。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-117">You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS.</span></span> <span data-ttu-id="3e3f1-118">例如，在特定版本的 Windows 中引進的通知類型，對於舊版 Windows 而言是未知的。</span><span class="sxs-lookup"><span data-stu-id="3e3f1-118">For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e3f1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e3f1-119">See also</span></span>

<span data-ttu-id="3e3f1-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="3e3f1-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>