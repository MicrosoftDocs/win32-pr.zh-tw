---
description: GetIID 方法會抓取將在其上執行方法之介面 (IID) 的介面識別碼。
ms.assetid: d6eb7d46-294a-4169-96d3-4bed02c48c08
title: 'CDeferredCommand. GetIID 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetIID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8677c70ab9c2c04224194bd825b106d33de8893
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994898"
---
# <a name="cdeferredcommandgetiid-method"></a><span data-ttu-id="9a257-103">CDeferredCommand. GetIID 方法</span><span class="sxs-lookup"><span data-stu-id="9a257-103">CDeferredCommand.GetIID method</span></span>

<span data-ttu-id="9a257-104">`GetIID`方法會針對將在其上執行方法的介面， (IID) 來抓取介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a257-104">The `GetIID` method retrieves the interface identifier (IID) of the interface on which the method will be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a257-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a257-105">Syntax</span></span>


```C++
REFIID GetIID();
```



## <a name="parameters"></a><span data-ttu-id="9a257-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a257-106">Parameters</span></span>

<span data-ttu-id="9a257-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9a257-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a257-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a257-108">Return value</span></span>

<span data-ttu-id="9a257-109">傳回將在其上執行方法之介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="9a257-109">Returns the IID of the interface on which the method will be run.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a257-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a257-110">Requirements</span></span>



| <span data-ttu-id="9a257-111">需求</span><span class="sxs-lookup"><span data-stu-id="9a257-111">Requirement</span></span> | <span data-ttu-id="9a257-112">值</span><span class="sxs-lookup"><span data-stu-id="9a257-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a257-113">標頭</span><span class="sxs-lookup"><span data-stu-id="9a257-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9a257-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9a257-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a257-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a257-115">Library</span></span><br/> | <dl> <span data-ttu-id="9a257-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9a257-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a257-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a257-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a257-118">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="9a257-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




