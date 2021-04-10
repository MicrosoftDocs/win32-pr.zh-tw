---
title: DXCoreNotificationType
description: 定義常數，指定 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件所引發的通知類型。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3eacd77d2cf15c78a0dc959285874de943fd9130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092817"
---
# <a name="dxcorenotificationtype-enum"></a><span data-ttu-id="9bce7-103">DXCoreNotificationType 列舉</span><span class="sxs-lookup"><span data-stu-id="9bce7-103">DXCoreNotificationType enum</span></span>

<span data-ttu-id="9bce7-104">定義常數，指定 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件所引發的通知類型。</span><span class="sxs-lookup"><span data-stu-id="9bce7-104">Defines constants that specify types of notifications raised by [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) objects.</span></span>

<span data-ttu-id="9bce7-105">您可以分別呼叫 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) 和 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)，來註冊及取消註冊這些通知。</span><span class="sxs-lookup"><span data-stu-id="9bce7-105">You can register and unregister for these notifications by calling [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) and [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bce7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bce7-106">Syntax</span></span>

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a><span data-ttu-id="9bce7-107">常數</span><span class="sxs-lookup"><span data-stu-id="9bce7-107">Constants</span></span>

### <a name="adapterliststale"></a><span data-ttu-id="9bce7-108">AdapterListStale</span><span class="sxs-lookup"><span data-stu-id="9bce7-108">AdapterListStale</span></span>

<span data-ttu-id="9bce7-109">當介面卡清單變得過時時， <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> 物件會引發這項通知。</span><span class="sxs-lookup"><span data-stu-id="9bce7-109">This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> object when the adapter list becomes stale.</span></span> <span data-ttu-id="9bce7-110">最新到過時的轉換是單向的，一次，因此最多隻會引發一次這項通知。</span><span class="sxs-lookup"><span data-stu-id="9bce7-110">The fresh-to-stale transition is one-way, and one-time, so this notification is raised at most one time.</span></span>

### <a name="adapternolongervalid"></a><span data-ttu-id="9bce7-111">AdapterNoLongerValid</span><span class="sxs-lookup"><span data-stu-id="9bce7-111">AdapterNoLongerValid</span></span>

<span data-ttu-id="9bce7-112">當介面卡不再有效時， <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> 物件就會引發此通知。</span><span class="sxs-lookup"><span data-stu-id="9bce7-112">This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> object when the adapter becomes no longer valid.</span></span> <span data-ttu-id="9bce7-113">有效轉換不正確轉換是單向的，而這項通知最多隻會引發一次。</span><span class="sxs-lookup"><span data-stu-id="9bce7-113">The valid-to-invalid transition is one-way, and one-time, so this notification is raised at most one time.</span></span>

### <a name="adapterbudgetchange"></a><span data-ttu-id="9bce7-114">AdapterBudgetChange</span><span class="sxs-lookup"><span data-stu-id="9bce7-114">AdapterBudgetChange</span></span>

<span data-ttu-id="9bce7-115">此通知是在介面卡預算變更發生時由 <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> 物件引發。</span><span class="sxs-lookup"><span data-stu-id="9bce7-115">This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> object when an adapter budget change occurs.</span></span> <span data-ttu-id="9bce7-116">此通知可能會發生多次。</span><span class="sxs-lookup"><span data-stu-id="9bce7-116">This notification can occur many times.</span></span> <span data-ttu-id="9bce7-117">使用此通知的功能與 <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3：： RegisterVideoMemoryBudgetChangeNotificationEvent</a>類似。</span><span class="sxs-lookup"><span data-stu-id="9bce7-117">Using this notification is functionally similar to <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent</a>.</span></span> <span data-ttu-id="9bce7-118">若要回應此事件，您應該呼叫 [IDXCoreAdapter：： QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (搭配 [DXCoreAdapterState：： AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) 來評估目前的記憶體預算狀態。</span><span class="sxs-lookup"><span data-stu-id="9bce7-118">In response to this event, you should call [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (with [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) to evaluate the current memory budget state.</span></span>

### <a name="adapterhardwarecontentprotectionteardown"></a><span data-ttu-id="9bce7-119">AdapterHardwareContentProtectionTeardown</span><span class="sxs-lookup"><span data-stu-id="9bce7-119">AdapterHardwareContentProtectionTeardown</span></span>

<span data-ttu-id="9bce7-120"><a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a>物件會引發此通知，以通知介面卡的硬體內容保護卸載。</span><span class="sxs-lookup"><span data-stu-id="9bce7-120">This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> object to notify of an adapter's hardware content protection teardown.</span></span> <span data-ttu-id="9bce7-121">此通知可能會發生多次。</span><span class="sxs-lookup"><span data-stu-id="9bce7-121">This notification can occur many times.</span></span> <span data-ttu-id="9bce7-122">其功能類似于 <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3：： RegisterHardwareContentProtectionTeardownStatusEvent</a>。</span><span class="sxs-lookup"><span data-stu-id="9bce7-122">It is functionally similar to <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a>.</span></span> <span data-ttu-id="9bce7-123">為了回應此事件，您應該重新評估目前的加密會話狀態;例如，藉由呼叫 [ID3D11VideoCoNtext1：： CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) 來判斷特定 [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) 介面之硬體清除的影響。</span><span class="sxs-lookup"><span data-stu-id="9bce7-123">In response to this event, you should re-evaluate the current crypto session status; for example, by calling [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) to determine the impact of the hardware teardown for a specific [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bce7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bce7-124">See also</span></span>

<span data-ttu-id="9bce7-125">[IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)、 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)、 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="9bce7-125">[IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>