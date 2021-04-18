---
title: IDXCoreAdapter::IsPropertySupported
description: 判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援指定的介面卡屬性。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968917"
---
# <a name="idxcoreadapterispropertysupported-method"></a><span data-ttu-id="66a56-103">IDXCoreAdapter：： IsPropertySupported 方法</span><span class="sxs-lookup"><span data-stu-id="66a56-103">IDXCoreAdapter::IsPropertySupported method</span></span>

<span data-ttu-id="66a56-104">判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援指定的介面卡屬性。</span><span class="sxs-lookup"><span data-stu-id="66a56-104">Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a56-105">語法</span><span class="sxs-lookup"><span data-stu-id="66a56-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="66a56-106">參數</span><span class="sxs-lookup"><span data-stu-id="66a56-106">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="66a56-107">屬性</span><span class="sxs-lookup"><span data-stu-id="66a56-107">property</span></span>

<span data-ttu-id="66a56-108">類型： **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="66a56-108">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="66a56-109">您要查詢之支援的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="66a56-109">The type of property that you're querying about support for.</span></span> <span data-ttu-id="66a56-110">如需每個介面卡屬性的詳細資訊，請參閱 [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="66a56-110">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="66a56-111">傳回</span><span class="sxs-lookup"><span data-stu-id="66a56-111">Returns</span></span>

<span data-ttu-id="66a56-112">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="66a56-112">Type: **bool**</span></span>

<span data-ttu-id="66a56-113"> `true`   如果這個 DXCore 介面卡物件和目前作業系統 (作業系統) 支援指定的介面卡屬性，則會傳回。</span><span class="sxs-lookup"><span data-stu-id="66a56-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span> <span data-ttu-id="66a56-114">否則，會傳回  `false` 。</span><span class="sxs-lookup"><span data-stu-id="66a56-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="66a56-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66a56-115">See also</span></span>

<span data-ttu-id="66a56-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="66a56-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>