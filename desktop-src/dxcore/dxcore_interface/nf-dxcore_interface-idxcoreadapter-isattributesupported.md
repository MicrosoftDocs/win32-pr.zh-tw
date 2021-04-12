---
title: IDXCoreAdapter::IsAttributeSupported
description: 判斷這個 DXCore 介面卡物件是否支援指定的介面卡屬性。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375604"
---
# <a name="idxcoreadapterisattributesupported-method"></a><span data-ttu-id="27e9a-103">IDXCoreAdapter：： IsAttributeSupported 方法</span><span class="sxs-lookup"><span data-stu-id="27e9a-103">IDXCoreAdapter::IsAttributeSupported method</span></span>

<span data-ttu-id="27e9a-104">判斷這個 DXCore 介面卡物件是否支援指定的介面卡屬性。</span><span class="sxs-lookup"><span data-stu-id="27e9a-104">Determines whether this DXCore adapter object supports the specified adapter attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e9a-105">語法</span><span class="sxs-lookup"><span data-stu-id="27e9a-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a><span data-ttu-id="27e9a-106">參數</span><span class="sxs-lookup"><span data-stu-id="27e9a-106">Parameters</span></span>

### <a name="attributeguid"></a><span data-ttu-id="27e9a-107">attributeGUID</span><span class="sxs-lookup"><span data-stu-id="27e9a-107">attributeGUID</span></span>

<span data-ttu-id="27e9a-108">類型： **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="27e9a-108">Type: **REFGUID**</span></span>

<span data-ttu-id="27e9a-109">介面卡屬性 GUID 的參考。</span><span class="sxs-lookup"><span data-stu-id="27e9a-109">A reference to an adapter attribute GUID.</span></span> <span data-ttu-id="27e9a-110">如需屬性 Guid 清單，請參閱 [DXCore adapter 屬性 guid](../dxcore-adapter-attribute-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="27e9a-110">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span>

## <a name="returns"></a><span data-ttu-id="27e9a-111">傳回</span><span class="sxs-lookup"><span data-stu-id="27e9a-111">Returns</span></span>

<span data-ttu-id="27e9a-112">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="27e9a-112">Type: **bool**</span></span>

<span data-ttu-id="27e9a-113"> `true`   如果這個 DXCore 介面卡物件支援指定的介面卡屬性，則傳回。</span><span class="sxs-lookup"><span data-stu-id="27e9a-113">Returns `true` if this DXCore adapter object supports the specified adapter attribute.</span></span> <span data-ttu-id="27e9a-114">否則，會傳回  `false` 。</span><span class="sxs-lookup"><span data-stu-id="27e9a-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="27e9a-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27e9a-115">See also</span></span>

<span data-ttu-id="27e9a-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="27e9a-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>