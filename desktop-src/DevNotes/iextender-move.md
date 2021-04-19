---
description: 移動 MDIForm、表單或控制項。
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: IExtender：： Move 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 2c7ed806629f0e5e1bb0cdee5c76910728fd651d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995047"
---
# <a name="iextendermove-method"></a><span data-ttu-id="521b7-103">IExtender：： Move 方法</span><span class="sxs-lookup"><span data-stu-id="521b7-103">IExtender::Move method</span></span>

<span data-ttu-id="521b7-104">移動 MDIForm、表單或控制項。</span><span class="sxs-lookup"><span data-stu-id="521b7-104">Moves an MDIForm, form, or control.</span></span>

## <a name="syntax"></a><span data-ttu-id="521b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="521b7-105">Syntax</span></span>


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a><span data-ttu-id="521b7-106">參數</span><span class="sxs-lookup"><span data-stu-id="521b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="521b7-107">*左方* \[在\]</span><span class="sxs-lookup"><span data-stu-id="521b7-107">*left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521b7-108">表單或控制項的左邊緣。</span><span class="sxs-lookup"><span data-stu-id="521b7-108">The left edge of the form or control.</span></span>

</dd> <dt>

<span data-ttu-id="521b7-109">*頂端* \[在\]</span><span class="sxs-lookup"><span data-stu-id="521b7-109">*top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521b7-110">表單或控制項的上邊緣。</span><span class="sxs-lookup"><span data-stu-id="521b7-110">The top edge of the form or control.</span></span>

</dd> <dt>

<span data-ttu-id="521b7-111">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="521b7-111">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521b7-112">表單或控制項的寬度。</span><span class="sxs-lookup"><span data-stu-id="521b7-112">The width of the form or control.</span></span>

</dd> <dt>

<span data-ttu-id="521b7-113">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="521b7-113">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521b7-114">表單或控制項的高度。</span><span class="sxs-lookup"><span data-stu-id="521b7-114">The height of the form or control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="521b7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="521b7-115">Return value</span></span>

<span data-ttu-id="521b7-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="521b7-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="521b7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="521b7-117">Requirements</span></span>



| <span data-ttu-id="521b7-118">需求</span><span class="sxs-lookup"><span data-stu-id="521b7-118">Requirement</span></span> | <span data-ttu-id="521b7-119">值</span><span class="sxs-lookup"><span data-stu-id="521b7-119">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="521b7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="521b7-120">DLL</span></span><br/> | <dl> <span data-ttu-id="521b7-121"><dt>Ole2disp.dll;</dt><dt>Oleaut32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="521b7-121"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="521b7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="521b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="521b7-123">**IExtender**</span><span class="sxs-lookup"><span data-stu-id="521b7-123">**IExtender**</span></span>](iextender.md)
</dt> </dl>

 

 




