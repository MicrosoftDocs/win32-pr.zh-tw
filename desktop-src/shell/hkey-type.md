---
description: 這些資料類型可以用來指定登錄值的型別。
title: '登錄資料類型 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992519"
---
# <a name="registry-data-types"></a><span data-ttu-id="0906d-103">登錄資料類型</span><span class="sxs-lookup"><span data-stu-id="0906d-103">Registry Data Types</span></span>

<span data-ttu-id="0906d-104">這些資料類型可以用來指定登錄值的型別。</span><span class="sxs-lookup"><span data-stu-id="0906d-104">These data types can be used to specify the type of a registry value.</span></span>



| <span data-ttu-id="0906d-105">常數</span><span class="sxs-lookup"><span data-stu-id="0906d-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="0906d-106">描述</span><span class="sxs-lookup"><span data-stu-id="0906d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <span data-ttu-id="0906d-107"><dt>**REG \_ 二進位檔**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-107"><dt>**REG\_BINARY**</dt></span></span> </dl>                                          | <span data-ttu-id="0906d-108">任何形式的二進位資料，</span><span class="sxs-lookup"><span data-stu-id="0906d-108">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <span data-ttu-id="0906d-109"><dt>**REG \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-109"><dt>**REG\_DWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="0906d-110">32位數位。</span><span class="sxs-lookup"><span data-stu-id="0906d-110">32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <span data-ttu-id="0906d-111"><dt>**REG \_ QWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-111"><dt>**REG\_QWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="0906d-112">64位數位。</span><span class="sxs-lookup"><span data-stu-id="0906d-112">64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <span data-ttu-id="0906d-113"><dt>**REG DWORD 位元組由大到 \_ \_ 小 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-113"><dt>**REG\_DWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="0906d-114">以位元組由大到小的格式的32位數位。</span><span class="sxs-lookup"><span data-stu-id="0906d-114">32-bit number in little-endian format.</span></span> <span data-ttu-id="0906d-115">這相當於 **REG \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="0906d-115">This is equivalent to **REG\_DWORD**.</span></span><br/> <span data-ttu-id="0906d-116">以位元組由小到大的格式來說，多位元組值會儲存在最低位元組的記憶體中， (「小端」 ) 到最高的位元組。</span><span class="sxs-lookup"><span data-stu-id="0906d-116">In little-endian format, a multibyte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="0906d-117">例如，值0x12345678 會儲存為 (0x78 0x56 0x34 0x12) 以位元組由小到大格式表示。</span><span class="sxs-lookup"><span data-stu-id="0906d-117">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span><br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <span data-ttu-id="0906d-118"><dt>**REG \_ QWORD 位元組由大到 \_ 小 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-118"><dt>**REG\_QWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="0906d-119">以位元組由大到小的格式的64位數位。</span><span class="sxs-lookup"><span data-stu-id="0906d-119">A 64-bit number in little-endian format.</span></span> <span data-ttu-id="0906d-120">這相當於 **REG \_ QWORD**。</span><span class="sxs-lookup"><span data-stu-id="0906d-120">This is equivalent to **REG\_QWORD**.</span></span> <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <span data-ttu-id="0906d-121"><dt>**REG \_ DWORD \_ BIG \_ ENDIAN**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-121"><dt>**REG\_DWORD\_BIG\_ENDIAN**</dt></span></span> </dl>          | <span data-ttu-id="0906d-122">以位元組由大到小的格式的32位數位。</span><span class="sxs-lookup"><span data-stu-id="0906d-122">32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="0906d-123">以位元組由大到小的格式，會將多位元組值儲存在記憶體中，從最大的位元組 (「大端」 ) 至最低位元組。</span><span class="sxs-lookup"><span data-stu-id="0906d-123">In big-endian format, a multibyte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="0906d-124">例如，值0x12345678 會以位元組由大到小的格式儲存為 (0x12 0x34 0x56 0x78) 。</span><span class="sxs-lookup"><span data-stu-id="0906d-124">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span><br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <span data-ttu-id="0906d-125"><dt>**REG \_ EXPAND \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-125"><dt>**REG\_EXPAND\_SZ**</dt></span></span> </dl>                                | <span data-ttu-id="0906d-126">以 Null 終止的字串，其中包含環境變數未展開的參考 (例如 "% PATH%" ) 。</span><span class="sxs-lookup"><span data-stu-id="0906d-126">Null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="0906d-127">它將會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。</span><span class="sxs-lookup"><span data-stu-id="0906d-127">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <span data-ttu-id="0906d-128"><dt>**REG \_ 連結**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-128"><dt>**REG\_LINK**</dt></span></span> </dl>                                                | <span data-ttu-id="0906d-129">Unicode 符號連結。</span><span class="sxs-lookup"><span data-stu-id="0906d-129">Unicode symbolic link.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <span data-ttu-id="0906d-130"><dt>**REG \_ 多重 \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-130"><dt>**REG\_MULTI\_SZ**</dt></span></span> </dl>                                   | <span data-ttu-id="0906d-131">以 null 結束的字串陣列，由兩個 null 字元終止。</span><span class="sxs-lookup"><span data-stu-id="0906d-131">Array of null-terminated strings that are terminated by two null characters.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <span data-ttu-id="0906d-132"><dt>**REG \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-132"><dt>**REG\_NONE**</dt></span></span> </dl>                                                | <span data-ttu-id="0906d-133">沒有定義的實值型別。</span><span class="sxs-lookup"><span data-stu-id="0906d-133">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <span data-ttu-id="0906d-134"><dt>**REG \_ 資源 \_ 清單**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-134"><dt>**REG\_RESOURCE\_LIST**</dt></span></span> </dl>                    | <span data-ttu-id="0906d-135">裝置驅動程式資源清單。</span><span class="sxs-lookup"><span data-stu-id="0906d-135">Device-driver resource list.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <span data-ttu-id="0906d-136"><dt>**REG \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-136"><dt>**REG\_SZ**</dt></span></span> </dl>                                                      | <span data-ttu-id="0906d-137">以 Null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="0906d-137">Null-terminated string.</span></span> <span data-ttu-id="0906d-138">它將會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。</span><span class="sxs-lookup"><span data-stu-id="0906d-138">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="0906d-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="0906d-139">Requirements</span></span>



| <span data-ttu-id="0906d-140">需求</span><span class="sxs-lookup"><span data-stu-id="0906d-140">Requirement</span></span> | <span data-ttu-id="0906d-141">值</span><span class="sxs-lookup"><span data-stu-id="0906d-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0906d-142">標頭</span><span class="sxs-lookup"><span data-stu-id="0906d-142">Header</span></span><br/> | <dl> <span data-ttu-id="0906d-143"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-143"><dt>Winnt.h</dt></span></span> </dl> |



 

 




