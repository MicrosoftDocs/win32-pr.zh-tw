---
title: 'Matrix5x4F 類別 (D2d1 \_ helper .h) '
description: Matrix5x4F 類別代表一系列的4個矩陣，並提供建立矩陣的便利方法。
ms.assetid: F014694B-5117-48E1-89F7-2F943515AEC6
keywords:
- Matrix5x4F 類別 Direct2D
- Matrix5x4F 類別 Direct2D，描述
topic_type:
- apiref
api_name:
- Matrix5x4F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 328214224f23b4afafc52d8eb2883a58b5bf2f38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467093"
---
# <a name="matrix5x4f-class"></a><span data-ttu-id="a0c8c-105">Matrix5x4F 類別</span><span class="sxs-lookup"><span data-stu-id="a0c8c-105">Matrix5x4F class</span></span>

<span data-ttu-id="a0c8c-106">**Matrix5x4F** 類別代表一系列的4個矩陣，並提供建立矩陣的便利方法。</span><span class="sxs-lookup"><span data-stu-id="a0c8c-106">The **Matrix5x4F** class represents a 5-by-4 matrix and provides convenience methods for creating matrices.</span></span>

## <a name="members"></a><span data-ttu-id="a0c8c-107">成員</span><span class="sxs-lookup"><span data-stu-id="a0c8c-107">Members</span></span>

<span data-ttu-id="a0c8c-108">**Matrix5x4F** 類別繼承自 [**D2D1 \_ 矩陣 \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)。</span><span class="sxs-lookup"><span data-stu-id="a0c8c-108">The **Matrix5x4F** class inherits from [**D2D1\_MATRIX\_5X4\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f).</span></span> <span data-ttu-id="a0c8c-109">**Matrix5x4F** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a0c8c-109">**Matrix5x4F** also has these types of members:</span></span>

-   [<span data-ttu-id="a0c8c-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="a0c8c-110">Constructors</span></span>](#constructors)

### <a name="constructors"></a><span data-ttu-id="a0c8c-111">建構函式</span><span class="sxs-lookup"><span data-stu-id="a0c8c-111">Constructors</span></span>

<span data-ttu-id="a0c8c-112">**Matrix5x4F** 類別具有這些函式。</span><span class="sxs-lookup"><span data-stu-id="a0c8c-112">The **Matrix5x4F** class has these constructors.</span></span>



| <span data-ttu-id="a0c8c-113">建構函式</span><span class="sxs-lookup"><span data-stu-id="a0c8c-113">Constructor</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="a0c8c-114">描述</span><span class="sxs-lookup"><span data-stu-id="a0c8c-114">Description</span></span>                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0c8c-115">**Matrix5x4F ()**</span><span class="sxs-lookup"><span data-stu-id="a0c8c-115">**Matrix5x4F()**</span></span>](matrix5x4f-matrix5x4f--.md)                                                                                                                                                                                                                                                       | <span data-ttu-id="a0c8c-116">將未初始化之 **Matrix5x4F** 類別的新實例具現化。</span><span class="sxs-lookup"><span data-stu-id="a0c8c-116">Instantiates a new instance of an uninitialized **Matrix5x4F** class.</span></span><br/>                                                   |
| [<span data-ttu-id="a0c8c-117">**Matrix5x4F (FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，FLOAT，float，float，float，float，float，float)  (FLOAT，float，float，float，float，float，float，float，float，float，float，float，float，float，float)**</span><span class="sxs-lookup"><span data-stu-id="a0c8c-117">**Matrix5x4F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)**</span></span>](matrix5x4f-matrix5x4f-floats-.md) | <span data-ttu-id="a0c8c-118">具現化 **Matrix5x4F** 類別的新實例，這個實例會使用所有浮點數矩陣值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="a0c8c-118">Instantiates a new instance of a **Matrix5x4F** class that is initialized with all of the floating point matrix values.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0c8c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0c8c-119">Requirements</span></span>



| <span data-ttu-id="a0c8c-120">需求</span><span class="sxs-lookup"><span data-stu-id="a0c8c-120">Requirement</span></span> | <span data-ttu-id="a0c8c-121">值</span><span class="sxs-lookup"><span data-stu-id="a0c8c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c8c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0c8c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a0c8c-123">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="a0c8c-123">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a0c8c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0c8c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a0c8c-125">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0c8c-125">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a0c8c-126">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="a0c8c-126">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a0c8c-127">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0c8c-127">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="a0c8c-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0c8c-128">Namespace</span></span><br/>                | <span data-ttu-id="a0c8c-129">D2D1</span><span class="sxs-lookup"><span data-stu-id="a0c8c-129">D2D1</span></span><br/>                                                                                                                          |
| <span data-ttu-id="a0c8c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a0c8c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0c8c-131"><dt>D2d1 \_ helper。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0c8c-131"><dt>D2d1\_helper.h</dt></span></span> </dl>                                                |
| <span data-ttu-id="a0c8c-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="a0c8c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0c8c-133"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0c8c-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="a0c8c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a0c8c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0c8c-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0c8c-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



## <a name="see-also"></a><span data-ttu-id="a0c8c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0c8c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c8c-137">**D2D1 \_ 矩陣 \_ 5X4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="a0c8c-137">**D2D1\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)
</dt> </dl>

 

 





