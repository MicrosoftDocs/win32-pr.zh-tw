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
# <a name="side-by-side-assembly-enumerations"></a>並存元件列舉

並存元件 API 會使用下列列舉。



| 列舉型別                                                         | 描述                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ASM \_ CMP \_ 旗標**](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | 由 [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) 方法用來指定要比較的兩個元件名稱部分。                                                                       |
| [**ASM \_ 顯示 \_ 旗標**](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | 由 [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) 方法用來指定要在名稱的字串表示中包含的並存元件名稱部分。 |
| [**ASM \_ 名稱**](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | 並存元件名稱中的名稱/值組的屬性識別碼。                                                                                                                    |
| [**建立 \_ ASM \_ 名稱 \_ OBJ \_ 旗標**](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | 由 [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) 函數用來指定並存元件名稱。                                                               |



 

 

 



