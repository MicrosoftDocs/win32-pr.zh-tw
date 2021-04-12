---
description: 使用以 null 結束的字串時，您的 Unicode 應用程式應該一律將零轉換成 TCHAR。
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: 使用以 Null 結尾的字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195431"
---
# <a name="using-null-terminated-strings"></a><span data-ttu-id="32164-103">使用以 Null 結尾的字串</span><span class="sxs-lookup"><span data-stu-id="32164-103">Using Null-terminated Strings</span></span>

<span data-ttu-id="32164-104">使用以 null 結束的字串時，您的 Unicode 應用程式應該一律將零轉換成 TCHAR。</span><span class="sxs-lookup"><span data-stu-id="32164-104">Your Unicode applications should always cast zero to TCHAR when using null-terminated strings.</span></span> <span data-ttu-id="32164-105">程式碼0x0000 是以 null 終止之字串的 Unicode 字串結束字元。</span><span class="sxs-lookup"><span data-stu-id="32164-105">The code 0x0000 is the Unicode string terminator for a null-terminated string.</span></span> <span data-ttu-id="32164-106">單一 null 位元組對此程式碼而言不足，因為許多 Unicode 字元都包含 null 位元組做為高或低位元組。</span><span class="sxs-lookup"><span data-stu-id="32164-106">A single null byte is not sufficient for this code, because many Unicode characters contain null bytes as either the high or the low byte.</span></span> <span data-ttu-id="32164-107">其中一個範例是字母 A，其字元碼為0x0041。</span><span class="sxs-lookup"><span data-stu-id="32164-107">An example is the letter A, for which the character code is 0x0041.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32164-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="32164-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32164-109">使用 Unicode 中的特殊字元</span><span class="sxs-lookup"><span data-stu-id="32164-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



