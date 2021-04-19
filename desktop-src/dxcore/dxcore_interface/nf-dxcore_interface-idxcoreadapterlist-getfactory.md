---
title: IDXCoreAdapterList::GetFactory
description: 抓取 DXCore 介面卡 factory 物件的 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面指標。 |IDXCoreAdapterList::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993813"
---
# <a name="idxcoreadapterlistgetfactory-method"></a><span data-ttu-id="4244e-104">IDXCoreAdapterList：： GetFactory 方法</span><span class="sxs-lookup"><span data-stu-id="4244e-104">IDXCoreAdapterList::GetFactory method</span></span>

<span data-ttu-id="4244e-105">抓取 DXCore 介面卡 factory 物件的 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="4244e-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="4244e-106">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="4244e-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4244e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4244e-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="4244e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4244e-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="4244e-109">riid</span><span class="sxs-lookup"><span data-stu-id="4244e-109">riid</span></span>

<span data-ttu-id="4244e-110">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="4244e-110">Type: **REFIID**</span></span>

<span data-ttu-id="4244e-111">全域唯一識別碼的參考， (您想要在 *ppvFactory* 中傳回之介面的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="4244e-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="4244e-112">這應該是 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)的介面識別碼 (IID) 。</span><span class="sxs-lookup"><span data-stu-id="4244e-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="4244e-113">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="4244e-113">ppvFactory [out]</span></span>

<span data-ttu-id="4244e-114">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="4244e-114">Type: **void\*\***</span></span>

<span data-ttu-id="4244e-115">具有在 *riid* 參數中指定之 IID 之介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="4244e-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="4244e-116">在成功傳回時， *\* ppvFactory* (已取值的位址) 包含現有 DXCore 介面卡 factory 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4244e-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="4244e-117">在傳回之前，函式會遞增 factory 物件之 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="4244e-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="4244e-118">傳回</span><span class="sxs-lookup"><span data-stu-id="4244e-118">Returns</span></span>

<span data-ttu-id="4244e-119">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="4244e-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="4244e-120">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="4244e-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="4244e-121">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="4244e-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="4244e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="4244e-122">Return value</span></span>|<span data-ttu-id="4244e-123">描述</span><span class="sxs-lookup"><span data-stu-id="4244e-123">Description</span></span>|
|-|-|
|<span data-ttu-id="4244e-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="4244e-124">E_NOINTERFACE</span></span>|<span data-ttu-id="4244e-125">針對 *riid* 提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="4244e-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="4244e-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="4244e-126">E_POINTER</span></span>|<span data-ttu-id="4244e-127">`nullptr` 是為 *ppvFactory* 所提供。</span><span class="sxs-lookup"><span data-stu-id="4244e-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4244e-128">備註</span><span class="sxs-lookup"><span data-stu-id="4244e-128">Remarks</span></span>

<span data-ttu-id="4244e-129">在 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 介面或 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 介面上存在參考的時間內，對 [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md)、 [IDXCoreAdapterList：： GetFactory]()或 [IDXCoreAdapter：： GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) 的其他呼叫會傳回相同物件的指標，並增加 **IDXCoreAdapterFactory** 介面的參考計數。</span><span class="sxs-lookup"><span data-stu-id="4244e-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](), or [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="4244e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4244e-130">See also</span></span>

<span data-ttu-id="4244e-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="4244e-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
