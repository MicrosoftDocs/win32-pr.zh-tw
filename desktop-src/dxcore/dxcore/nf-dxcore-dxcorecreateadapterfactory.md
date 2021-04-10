---
title: DXCoreCreateAdapterFactory
description: 建立可用來產生進一步 DXCore 物件的 DXCore 介面卡 factory。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933492"
---
# <a name="dxcorecreateadapterfactory-function"></a><span data-ttu-id="a203c-103">DXCoreCreateAdapterFactory 函式</span><span class="sxs-lookup"><span data-stu-id="a203c-103">DXCoreCreateAdapterFactory function</span></span>

## <a name="description"></a><span data-ttu-id="a203c-104">Description</span><span class="sxs-lookup"><span data-stu-id="a203c-104">Description</span></span>

<span data-ttu-id="a203c-105">建立可用來產生進一步 DXCore 物件的 DXCore 介面卡 factory。</span><span class="sxs-lookup"><span data-stu-id="a203c-105">Creates a DXCore adapter factory, which you can use to generate further DXCore objects.</span></span> <span data-ttu-id="a203c-106">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="a203c-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="a203c-107">參數</span><span class="sxs-lookup"><span data-stu-id="a203c-107">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="a203c-108">riid</span><span class="sxs-lookup"><span data-stu-id="a203c-108">riid</span></span>

<span data-ttu-id="a203c-109">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="a203c-109">Type: **REFIID**</span></span>

<span data-ttu-id="a203c-110">全域唯一識別碼的參考， (您想要在 *ppvFactory* 中傳回之介面的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="a203c-110">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="a203c-111">這應該是 [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)的介面識別碼 (IID) 。</span><span class="sxs-lookup"><span data-stu-id="a203c-111">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="a203c-112">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="a203c-112">ppvFactory [out]</span></span>

<span data-ttu-id="a203c-113">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="a203c-113">Type: **void\*\***</span></span>

<span data-ttu-id="a203c-114">具有在 *riid* 參數中指定之 IID 之介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="a203c-114">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="a203c-115">在成功傳回時， *\* ppvFactory* (已取值的位址) 包含已建立之 DXCore factory 的指標。</span><span class="sxs-lookup"><span data-stu-id="a203c-115">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the DXCore factory created.</span></span>

## <a name="returns"></a><span data-ttu-id="a203c-116">傳回</span><span class="sxs-lookup"><span data-stu-id="a203c-116">Returns</span></span>

<span data-ttu-id="a203c-117">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="a203c-117">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="a203c-118">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="a203c-118">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a203c-119">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="a203c-119">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="a203c-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="a203c-120">Return value</span></span>|<span data-ttu-id="a203c-121">描述</span><span class="sxs-lookup"><span data-stu-id="a203c-121">Description</span></span>|
|-|-|
|<span data-ttu-id="a203c-122">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="a203c-122">E_NOINTERFACE</span></span>|<span data-ttu-id="a203c-123">針對 *riid* 提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="a203c-123">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="a203c-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="a203c-124">E_POINTER</span></span>|<span data-ttu-id="a203c-125">`nullptr` 是為 *ppvFactory* 所提供。</span><span class="sxs-lookup"><span data-stu-id="a203c-125">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a203c-126">備註</span><span class="sxs-lookup"><span data-stu-id="a203c-126">Remarks</span></span>

<span data-ttu-id="a203c-127">在 [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) 介面、 [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) 介面或 [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) 介面上存在參考的時間內，對 **DXCoreCreateAdapterFactory**、 [IDXCoreAdapterList：： GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)或 [IDXCoreAdapter：： GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) 的其他呼叫會傳回相同物件的指標，並增加 **IDXCoreAdapterFactory** 介面的參考計數。</span><span class="sxs-lookup"><span data-stu-id="a203c-127">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="a203c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a203c-128">See also</span></span>

<span data-ttu-id="a203c-129">[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a203c-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>