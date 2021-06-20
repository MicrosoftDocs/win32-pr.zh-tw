---
description: 深入瞭解並存元件 API 中使用的列舉，例如 ASM_CMP_FLAGS 和 CREATE_ASM_NAME_OBJ_FLAGS。
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: 並存元件列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f393ab9d8657ecaa52cad555dad5a831699687
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404741"
---
# <a name="side-by-side-assembly-enumerations"></a><span data-ttu-id="fecfd-103">並存元件列舉</span><span class="sxs-lookup"><span data-stu-id="fecfd-103">Side-by-Side Assembly Enumerations</span></span>

<span data-ttu-id="fecfd-104">並存元件 API 會使用下列列舉。</span><span class="sxs-lookup"><span data-stu-id="fecfd-104">The side-by-side assembly API uses the following enumerations.</span></span>



| <span data-ttu-id="fecfd-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="fecfd-105">Enumeration</span></span>                                                         | <span data-ttu-id="fecfd-106">描述</span><span class="sxs-lookup"><span data-stu-id="fecfd-106">Description</span></span>                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fecfd-107">**ASM \_ CMP \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="fecfd-107">**ASM\_CMP\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | <span data-ttu-id="fecfd-108">由 [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) 方法用來指定要比較的兩個元件名稱部分。</span><span class="sxs-lookup"><span data-stu-id="fecfd-108">Used by the [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) method to specify which parts of two assembly names to compare.</span></span>                                                                       |
| [<span data-ttu-id="fecfd-109">**ASM \_ 顯示 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="fecfd-109">**ASM\_DISPLAY\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | <span data-ttu-id="fecfd-110">由 [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) 方法用來指定要在名稱的字串表示中包含的並存元件名稱部分。</span><span class="sxs-lookup"><span data-stu-id="fecfd-110">Used by the [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) method to specify which portions of the side-by-side assembly name to include in the string representation of the name.</span></span> |
| [<span data-ttu-id="fecfd-111">**ASM \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="fecfd-111">**ASM\_NAME**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | <span data-ttu-id="fecfd-112">並存元件名稱中的名稱/值組的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="fecfd-112">Property IDs for the name-value pairs in an side-by-side assembly name.</span></span>                                                                                                                    |
| [<span data-ttu-id="fecfd-113">**建立 \_ ASM \_ 名稱 \_ OBJ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="fecfd-113">**CREATE\_ASM\_NAME\_OBJ\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | <span data-ttu-id="fecfd-114">由 [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) 函數用來指定並存元件名稱。</span><span class="sxs-lookup"><span data-stu-id="fecfd-114">Used by the [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) function to specify the side-by-side assembly name.</span></span>                                                               |



 

 

 



