---
description: 指定屬性在指定時間所假設的值。
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: 'DEXTER_PARAM 結構 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000411"
---
# <a name="dexter_param-structure"></a><span data-ttu-id="f4cab-103">DEXTER \_ PARAM 結構</span><span class="sxs-lookup"><span data-stu-id="f4cab-103">DEXTER\_PARAM structure</span></span>

> [!Note]  
> <span data-ttu-id="f4cab-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="f4cab-104">\[Deprecated.</span></span> <span data-ttu-id="f4cab-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="f4cab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f4cab-106">指定屬性在指定時間所假設的值。</span><span class="sxs-lookup"><span data-stu-id="f4cab-106">Specifies the value that a property assumes at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cab-107">語法</span><span class="sxs-lookup"><span data-stu-id="f4cab-107">Syntax</span></span>


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a><span data-ttu-id="f4cab-108">成員</span><span class="sxs-lookup"><span data-stu-id="f4cab-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4cab-109">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f4cab-109">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f4cab-110">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4cab-110">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="f4cab-111">**dispID**</span><span class="sxs-lookup"><span data-stu-id="f4cab-111">**dispID**</span></span>
</dt> <dd>

<span data-ttu-id="f4cab-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="f4cab-112">Reserved.</span></span> <span data-ttu-id="f4cab-113">設定為零。</span><span class="sxs-lookup"><span data-stu-id="f4cab-113">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f4cab-114">**\N**</span><span class="sxs-lookup"><span data-stu-id="f4cab-114">**nValues**</span></span>
</dt> <dd>

<span data-ttu-id="f4cab-115">屬性所採用的值數目。</span><span class="sxs-lookup"><span data-stu-id="f4cab-115">Number of values that the property assumes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4cab-116">備註</span><span class="sxs-lookup"><span data-stu-id="f4cab-116">Remarks</span></span>

<span data-ttu-id="f4cab-117">物件必須支援 **IDispatch** 介面。</span><span class="sxs-lookup"><span data-stu-id="f4cab-117">The object must support the **IDispatch** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4cab-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4cab-118">Requirements</span></span>



| <span data-ttu-id="f4cab-119">需求</span><span class="sxs-lookup"><span data-stu-id="f4cab-119">Requirement</span></span> | <span data-ttu-id="f4cab-120">值</span><span class="sxs-lookup"><span data-stu-id="f4cab-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cab-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f4cab-121">Header</span></span><br/> | <dl> <span data-ttu-id="f4cab-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4cab-122"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4cab-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4cab-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4cab-124">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="f4cab-124">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="f4cab-125">**DEXTER \_ 值**</span><span class="sxs-lookup"><span data-stu-id="f4cab-125">**DEXTER\_VALUE**</span></span>](dexter-value.md)
</dt> </dl>

 

 




