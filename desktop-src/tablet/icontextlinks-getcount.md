---
description: 取得此集合中的 ICoNtextLink 物件數目。
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'ICoNtextLinks：： GetCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191415"
---
# <a name="icontextlinksgetcount-method"></a><span data-ttu-id="91ae0-103">ICoNtextLinks：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="91ae0-103">IContextLinks::GetCount method</span></span>

<span data-ttu-id="91ae0-104">取得此集合中的 [**ICoNtextLink**](icontextlink.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="91ae0-104">Gets the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ae0-105">語法</span><span class="sxs-lookup"><span data-stu-id="91ae0-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="91ae0-106">參數</span><span class="sxs-lookup"><span data-stu-id="91ae0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ae0-107">*pulCount* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="91ae0-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="91ae0-108">包含在這個集合中的 [**ICoNtextLink**](icontextlink.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="91ae0-108">The number of [**IContextLink**](icontextlink.md) objects that are contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ae0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="91ae0-109">Return value</span></span>

<span data-ttu-id="91ae0-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="91ae0-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91ae0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="91ae0-111">Requirements</span></span>



| <span data-ttu-id="91ae0-112">需求</span><span class="sxs-lookup"><span data-stu-id="91ae0-112">Requirement</span></span> | <span data-ttu-id="91ae0-113">值</span><span class="sxs-lookup"><span data-stu-id="91ae0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ae0-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91ae0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="91ae0-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91ae0-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="91ae0-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91ae0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="91ae0-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="91ae0-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="91ae0-118">標頭</span><span class="sxs-lookup"><span data-stu-id="91ae0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ae0-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="91ae0-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="91ae0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="91ae0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91ae0-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91ae0-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="91ae0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91ae0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ae0-123">**ICoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="91ae0-123">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="91ae0-124">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="91ae0-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




