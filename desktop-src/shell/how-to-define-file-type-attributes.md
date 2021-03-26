---
description: 在登錄中定義檔案類型屬性。
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: 如何定義檔案類型屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849197"
---
# <a name="how-to-define-file-type-attributes"></a><span data-ttu-id="6653f-103">如何定義檔案類型屬性</span><span class="sxs-lookup"><span data-stu-id="6653f-103">How to Define File Type Attributes</span></span>

<span data-ttu-id="6653f-104">將檔案類型屬性指派給相關聯的 ProgID，可讓您控制檔案類型行為的某些層面。</span><span class="sxs-lookup"><span data-stu-id="6653f-104">Assigning file type attributes to an associated ProgID enables you to control some aspects of the file type's behavior.</span></span> <span data-ttu-id="6653f-105">在 Windows Vista 之前，這些屬性可讓您限制使用者可以使用 [ **資料夾選項** ] 屬性索引標籤的範圍，以修改檔案類型的各個層面，例如其圖示或動詞。</span><span class="sxs-lookup"><span data-stu-id="6653f-105">Prior to Windows Vista, these attributes could enable you to limit the extent to which the user could use the **Folder Options** property tab to modify various aspects of the file type, such as its icon or verbs.</span></span>

<span data-ttu-id="6653f-106">檔案類型屬性是二進位旗標，會在檔案類型相關聯的 ProgID 子機碼中指定為 **reg \_ DWORD** 或 **reg \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="6653f-106">File type attributes are binary flags specified as **REG\_DWORD** or **REG\_BINARY** values in the file type's associated ProgID subkey.</span></span>

<span data-ttu-id="6653f-107">若要指派檔案類型的屬性，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6653f-107">To assign attributes for a file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="6653f-108">指示</span><span class="sxs-lookup"><span data-stu-id="6653f-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="6653f-109">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="6653f-109">Step 1:</span></span>

<span data-ttu-id="6653f-110">將 EditFlags 專案新增至檔案類型的相關 ProgID 子機碼。</span><span class="sxs-lookup"><span data-stu-id="6653f-110">Add an EditFlags entry to the file type's associated ProgID subkey.</span></span>

### <a name="step-2"></a><span data-ttu-id="6653f-111">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="6653f-111">Step 2:</span></span>

<span data-ttu-id="6653f-112">將專案設定為適當的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6653f-112">Set the entry to the appropriate attribute value.</span></span>

<span data-ttu-id="6653f-113">下列範例顯示 FTA \_ NoRemove (0x00000010) 和 FTA \_ NoNewVerb (0x00000020) 屬性為 myp 檔案類型設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="6653f-113">The following example shows the FTA\_NoRemove (0x00000010) and FTA\_NoNewVerb (0x00000020) attributes set for the .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a><span data-ttu-id="6653f-114">備註</span><span class="sxs-lookup"><span data-stu-id="6653f-114">Remarks</span></span>

<span data-ttu-id="6653f-115">旗標可以與邏輯 OR 結合，以形成單一屬性值。</span><span class="sxs-lookup"><span data-stu-id="6653f-115">The flags can be combined with a logical OR to form the single attribute value.</span></span>

<span data-ttu-id="6653f-116">如需可能的檔案類型屬性和其十六進位值的清單，以及以程式設計方式取得和設定這些值的詳細資訊，請參閱 [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags)。</span><span class="sxs-lookup"><span data-stu-id="6653f-116">For a list of possible file type attributes and their hexadecimal values, and more details on programmatically retrieving and setting these values, see [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span></span>

 

 



