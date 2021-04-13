---
title: IDXCoreAdapter::IsSetStateSupported
description: 判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援設定指定介面卡狀態的值。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 284e38a622c882fce04278d9134908f55c9a25cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376169"
---
# <a name="idxcoreadapterissetstatesupported-method"></a><span data-ttu-id="9730c-103">IDXCoreAdapter：： IsSetStateSupported 方法</span><span class="sxs-lookup"><span data-stu-id="9730c-103">IDXCoreAdapter::IsSetStateSupported method</span></span>

<span data-ttu-id="9730c-104">判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援設定指定介面卡狀態的值。</span><span class="sxs-lookup"><span data-stu-id="9730c-104">Determines whether this DXCore adapter object and the current operating system (OS) support setting the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9730c-105">語法</span><span class="sxs-lookup"><span data-stu-id="9730c-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="9730c-106">參數</span><span class="sxs-lookup"><span data-stu-id="9730c-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="9730c-107">狀態</span><span class="sxs-lookup"><span data-stu-id="9730c-107">state</span></span>

<span data-ttu-id="9730c-108">類型： **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="9730c-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="9730c-109">您所查詢的狀態專案的支援類型。</span><span class="sxs-lookup"><span data-stu-id="9730c-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="9730c-110">如需每個介面卡狀態種類的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="9730c-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="9730c-111">傳回</span><span class="sxs-lookup"><span data-stu-id="9730c-111">Returns</span></span>

<span data-ttu-id="9730c-112">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="9730c-112">Type: **bool**</span></span>

<span data-ttu-id="9730c-113"> `true`   如果這個 DXCore 介面卡物件和目前作業系統 (作業系統) 支援設定指定的介面卡狀態，則會傳回。</span><span class="sxs-lookup"><span data-stu-id="9730c-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support setting the specified adapter state.</span></span> <span data-ttu-id="9730c-114">否則，會傳回  `false` 。</span><span class="sxs-lookup"><span data-stu-id="9730c-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9730c-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9730c-115">See also</span></span>

<span data-ttu-id="9730c-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="9730c-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>