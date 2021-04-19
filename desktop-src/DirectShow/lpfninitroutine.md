---
description: 從 DLL 進入點呼叫之函式的指標。
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: 'LPFNInitRoutine 函式指標 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995282"
---
# <a name="lpfninitroutine-function-pointer"></a><span data-ttu-id="cf93f-103">LPFNInitRoutine 函式指標</span><span class="sxs-lookup"><span data-stu-id="cf93f-103">LPFNInitRoutine function pointer</span></span>

<span data-ttu-id="cf93f-104">從 DLL 進入點呼叫之函式的指標。</span><span class="sxs-lookup"><span data-stu-id="cf93f-104">Pointer to a function that gets called from the DLL entry point.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf93f-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf93f-105">Syntax</span></span>


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="cf93f-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf93f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf93f-107">*bLoading*</span><span class="sxs-lookup"><span data-stu-id="cf93f-107">*bLoading*</span></span> 
</dt> <dd>

<span data-ttu-id="cf93f-108">載入 DLL 時 **為 TRUE** ，卸載 dll 時為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="cf93f-108">**TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="cf93f-109">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="cf93f-109">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="cf93f-110">物件之 CLISD 的指標，在 [**CFactoryTemplate：： m \_ ClsID**](cfactorytemplate-m-clsid.md) 成員變數中指定。</span><span class="sxs-lookup"><span data-stu-id="cf93f-110">Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf93f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf93f-111">Return value</span></span>

<span data-ttu-id="cf93f-112">這個函式指標不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cf93f-112">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf93f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf93f-113">Requirements</span></span>



| <span data-ttu-id="cf93f-114">需求</span><span class="sxs-lookup"><span data-stu-id="cf93f-114">Requirement</span></span> | <span data-ttu-id="cf93f-115">值</span><span class="sxs-lookup"><span data-stu-id="cf93f-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf93f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="cf93f-116">Header</span></span><br/> | <dl> <span data-ttu-id="cf93f-117"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cf93f-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf93f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf93f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf93f-119">**CFactoryTemplate 類別**</span><span class="sxs-lookup"><span data-stu-id="cf93f-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




