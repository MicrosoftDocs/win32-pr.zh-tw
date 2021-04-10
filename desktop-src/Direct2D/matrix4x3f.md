---
title: 'Matrix4x3F 類別 (D2d1 \_ helper .h) '
description: Matrix4x3F 類別代表 4 x 3 的矩陣，並提供建立矩陣的便利方法。
ms.assetid: 633B1828-0CB5-4CD3-9826-C65083C6C0A9
keywords:
- Matrix4x3F 類別 Direct2D
- Matrix4x3F 類別 Direct2D，描述
topic_type:
- apiref
api_name:
- Matrix4x3F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81467b51eb22586d537c7ea8032e13a30da19c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844415"
---
# <a name="matrix4x3f-class"></a><span data-ttu-id="c623f-105">Matrix4x3F 類別</span><span class="sxs-lookup"><span data-stu-id="c623f-105">Matrix4x3F class</span></span>

<span data-ttu-id="c623f-106">**Matrix4x3F** 類別代表 4 x 3 的矩陣，並提供建立矩陣的便利方法。</span><span class="sxs-lookup"><span data-stu-id="c623f-106">The **Matrix4x3F** class represents a 4-by-3 matrix and provides convenience methods for creating matrices.</span></span>

## <a name="members"></a><span data-ttu-id="c623f-107">成員</span><span class="sxs-lookup"><span data-stu-id="c623f-107">Members</span></span>

<span data-ttu-id="c623f-108">**Matrix4x3F** 類別繼承自 [**D2D1 \_ 矩陣 \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)。</span><span class="sxs-lookup"><span data-stu-id="c623f-108">The **Matrix4x3F** class inherits from [**D2D1\_MATRIX\_4X3\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span></span> <span data-ttu-id="c623f-109">**Matrix4x3F** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c623f-109">**Matrix4x3F** also has these types of members:</span></span>

-   [<span data-ttu-id="c623f-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="c623f-110">Constructors</span></span>](#constructors)

### <a name="constructors"></a><span data-ttu-id="c623f-111">建構函式</span><span class="sxs-lookup"><span data-stu-id="c623f-111">Constructors</span></span>

<span data-ttu-id="c623f-112">**Matrix4x3F** 類別具有這些函式。</span><span class="sxs-lookup"><span data-stu-id="c623f-112">The **Matrix4x3F** class has these constructors.</span></span>



| <span data-ttu-id="c623f-113">建構函式</span><span class="sxs-lookup"><span data-stu-id="c623f-113">Constructor</span></span>                                                                                                                                                                                           | <span data-ttu-id="c623f-114">描述</span><span class="sxs-lookup"><span data-stu-id="c623f-114">Description</span></span>                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c623f-115">**Matrix4x3F ()**</span><span class="sxs-lookup"><span data-stu-id="c623f-115">**Matrix4x3F()**</span></span>](matrix4x3f-matrix4x3f--.md)                                                                                                                                                       | <span data-ttu-id="c623f-116">將未初始化之 **Matrix4x3F** 類別的新實例具現化。</span><span class="sxs-lookup"><span data-stu-id="c623f-116">Instantiates a new instance of an uninitialized **Matrix4x3F** class.</span></span><br/>                                                   |
| [<span data-ttu-id="c623f-117">**Matrix4x3F (FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT)  (FLOAT，FLOAT，float，float，float，float，float，float，float，float，float，FLOAT)**</span><span class="sxs-lookup"><span data-stu-id="c623f-117">**Matrix4x3F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)**</span></span>](matrix4x3f-matrix4x3f-floats-.md) | <span data-ttu-id="c623f-118">具現化 **Matrix4x3F** 類別的新實例，這個實例會使用所有浮點數矩陣值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="c623f-118">Instantiates a new instance of a **Matrix4x3F** class that is initialized with all of the floating point matrix values.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c623f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c623f-119">Requirements</span></span>



| <span data-ttu-id="c623f-120">需求</span><span class="sxs-lookup"><span data-stu-id="c623f-120">Requirement</span></span> | <span data-ttu-id="c623f-121">值</span><span class="sxs-lookup"><span data-stu-id="c623f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c623f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c623f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c623f-123">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="c623f-123">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c623f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c623f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c623f-125">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c623f-125">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c623f-126">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="c623f-126">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c623f-127">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c623f-127">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="c623f-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="c623f-128">Namespace</span></span><br/>                | <span data-ttu-id="c623f-129">D2D1</span><span class="sxs-lookup"><span data-stu-id="c623f-129">D2D1</span></span><br/>                                                                                                                          |
| <span data-ttu-id="c623f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c623f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c623f-131"><dt>D2d1 \_ helper。h</dt></span><span class="sxs-lookup"><span data-stu-id="c623f-131"><dt>D2d1\_helper.h</dt></span></span> </dl>                                                |
| <span data-ttu-id="c623f-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="c623f-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c623f-133"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c623f-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="c623f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c623f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c623f-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c623f-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



## <a name="see-also"></a><span data-ttu-id="c623f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c623f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c623f-137">**D2D1 \_ 矩陣 \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="c623f-137">**D2D1\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)
</dt> </dl>

 

 





