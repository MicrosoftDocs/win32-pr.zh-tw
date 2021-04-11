---
description: 針對 NLS，排序 (也稱為 &\# 0034; 定序&\# 0034; ) 是字串的相片順序。
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: '排序 (國際化) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195289"
---
# <a name="sorting"></a><span data-ttu-id="f0736-103">排序</span><span class="sxs-lookup"><span data-stu-id="f0736-103">Sorting</span></span>

<span data-ttu-id="f0736-104">針對 NLS，排序 (也稱為「定序」 ) 是字串的相片順序。</span><span class="sxs-lookup"><span data-stu-id="f0736-104">For NLS, sorting (also known as "collation") is the arrangement of strings.</span></span> <span data-ttu-id="f0736-105">排序有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="f0736-105">There are two types of sorting:</span></span>

-   <span data-ttu-id="f0736-106">語言排序。</span><span class="sxs-lookup"><span data-stu-id="f0736-106">Linguistic sorting.</span></span> <span data-ttu-id="f0736-107">依) 排序，將具有類似語言特性的字串排列成群組 (。</span><span class="sxs-lookup"><span data-stu-id="f0736-107">Arranges strings with similar linguistic characteristics into groups (by sorts).</span></span>
-   <span data-ttu-id="f0736-108">序數 (非語言) 排序。</span><span class="sxs-lookup"><span data-stu-id="f0736-108">Ordinal (non-linguistic) sorting.</span></span> <span data-ttu-id="f0736-109">依排序次序排列字串。</span><span class="sxs-lookup"><span data-stu-id="f0736-109">Arranges the strings in an ordered sequence.</span></span>

<span data-ttu-id="f0736-110">排序會使用 NLS 字串比較函式（例如 [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 和 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)）或「包裝函式」 API 函式（例如 [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa)），在內部呼叫 NLS 字串比較函數。</span><span class="sxs-lookup"><span data-stu-id="f0736-110">Sorting uses the NLS string comparison functions, such as [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) and [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), or "wrapper" API functions, such as [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), that internally call the NLS string comparison functions.</span></span>

<span data-ttu-id="f0736-111">如需在應用程式中執行排序的詳細資訊，請參閱 [在您的應用程式中處理排序](handling-sorting-in-your-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="f0736-111">For details about implementing sorting in your applications, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0736-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0736-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0736-113">關於國家語言支援</span><span class="sxs-lookup"><span data-stu-id="f0736-113">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f0736-114">處理應用程式中的排序</span><span class="sxs-lookup"><span data-stu-id="f0736-114">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="f0736-115">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="f0736-115">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[<span data-ttu-id="f0736-116">LCMapString</span><span class="sxs-lookup"><span data-stu-id="f0736-116">LCMapString</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
