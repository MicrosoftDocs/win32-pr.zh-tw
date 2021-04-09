---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: 判斷 OS 是否可瞭解指定的 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682542"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a><span data-ttu-id="1a09b-103">IDXCoreAdapterList：： IsAdapterPreferenceSupported 方法</span><span class="sxs-lookup"><span data-stu-id="1a09b-103">IDXCoreAdapterList::IsAdapterPreferenceSupported method</span></span>

## <a name="description"></a><span data-ttu-id="1a09b-104">Description</span><span class="sxs-lookup"><span data-stu-id="1a09b-104">Description</span></span>

<span data-ttu-id="1a09b-105">判斷目前作業系統 (作業系統) 是否瞭解指定的 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值。</span><span class="sxs-lookup"><span data-stu-id="1a09b-105">Determines whether a specified [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value is understood by the current operating system (OS).</span></span> <span data-ttu-id="1a09b-106">您可以在呼叫 [IDXCoreAdapterList：： Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)之前呼叫 **IsAdapterPreferenceSupported** 。</span><span class="sxs-lookup"><span data-stu-id="1a09b-106">You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a09b-107">語法</span><span class="sxs-lookup"><span data-stu-id="1a09b-107">Syntax</span></span>

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a><span data-ttu-id="1a09b-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a09b-108">Parameters</span></span>

### <a name="preference"></a><span data-ttu-id="1a09b-109">preference</span><span class="sxs-lookup"><span data-stu-id="1a09b-109">preference</span></span>

<span data-ttu-id="1a09b-110">類型： **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span><span class="sxs-lookup"><span data-stu-id="1a09b-110">Type: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span></span>

<span data-ttu-id="1a09b-111">系統會檢查 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值，以查看作業系統是否支援此值。</span><span class="sxs-lookup"><span data-stu-id="1a09b-111">A [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value that will be checked to see whether it's supported by the OS.</span></span>

## <a name="returns"></a><span data-ttu-id="1a09b-112">傳回</span><span class="sxs-lookup"><span data-stu-id="1a09b-112">Returns</span></span>

<span data-ttu-id="1a09b-113">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="1a09b-113">Type: **bool**</span></span>

<span data-ttu-id="1a09b-114">`true`如果目前的作業系統瞭解排序類型，則傳回。</span><span class="sxs-lookup"><span data-stu-id="1a09b-114">Returns `true` if the sort type is understood by the current OS.</span></span> <span data-ttu-id="1a09b-115">否則傳回 `false`。</span><span class="sxs-lookup"><span data-stu-id="1a09b-115">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a09b-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a09b-116">See also</span></span>

<span data-ttu-id="1a09b-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="1a09b-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>