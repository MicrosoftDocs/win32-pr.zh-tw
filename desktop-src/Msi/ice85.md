---
description: ICE85 會驗證 MoveFile 資料表的 [未使用] 資料行是否為有效的完整檔案名。 此欄位可包含萬用字元 (\* 和？ ) 。
ms.assetid: fce8c5cc-03b3-4dff-9648-ed137cfc5d1b
title: ICE85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96bf5115ea1e0351d7d1d1cc52140eb27d0ef333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114176"
---
# <a name="ice85"></a><span data-ttu-id="8e8a9-104">ICE85</span><span class="sxs-lookup"><span data-stu-id="8e8a9-104">ICE85</span></span>

<span data-ttu-id="8e8a9-105">ICE85 會驗證 [MoveFile 資料表](movefile-table.md) 的 [未使用] 資料行是否為有效的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="8e8a9-105">ICE85 validates that the SourceName column of the [MoveFile table](movefile-table.md) is a valid long file name.</span></span> <span data-ttu-id="8e8a9-106">此欄位可包含萬用字元 (\* 和？ ) 。</span><span class="sxs-lookup"><span data-stu-id="8e8a9-106">This field may contain wildcard characters (\* and ?).</span></span>

## <a name="result"></a><span data-ttu-id="8e8a9-107">結果</span><span class="sxs-lookup"><span data-stu-id="8e8a9-107">Result</span></span>

<span data-ttu-id="8e8a9-108">ICE85 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e8a9-108">ICE85 posts the following errors.</span></span>



| <span data-ttu-id="8e8a9-109">ICE85 錯誤</span><span class="sxs-lookup"><span data-stu-id="8e8a9-109">ICE85 error</span></span>                                                      | <span data-ttu-id="8e8a9-110">Description</span><span class="sxs-lookup"><span data-stu-id="8e8a9-110">Description</span></span>                                                              |
|------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="8e8a9-111">\[ \] 在 MoveFile 資料表中找到的「2」表格式不正確。</span><span class="sxs-lookup"><span data-stu-id="8e8a9-111">SourceName '\[2\]' found in the MoveFile table is of bad format.</span></span> | <span data-ttu-id="8e8a9-112">MoveFile 資料表中的未通過欄位不是有效的完整檔案名</span><span class="sxs-lookup"><span data-stu-id="8e8a9-112">The SourceName field in the MoveFile table is not a valid long file name</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8e8a9-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e8a9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e8a9-114">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="8e8a9-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



