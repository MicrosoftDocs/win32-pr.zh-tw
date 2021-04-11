---
description: 下列函數可讓您列舉受保護的資源。
ms.assetid: 6806c320-6071-4075-9003-2469089a9cc4
title: WRP 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966e25d0c9c78e384c38098b43826f1e6342c9b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945302"
---
# <a name="wrp-functions"></a><span data-ttu-id="1d1d0-103">WRP 函式</span><span class="sxs-lookup"><span data-stu-id="1d1d0-103">WRP Functions</span></span>

<span data-ttu-id="1d1d0-104">下列函數可讓您列舉受保護的資源。</span><span class="sxs-lookup"><span data-stu-id="1d1d0-104">The following functions allow you to enumerate protected resources.</span></span>



| <span data-ttu-id="1d1d0-105">函式</span><span class="sxs-lookup"><span data-stu-id="1d1d0-105">Function</span></span>                                         | <span data-ttu-id="1d1d0-106">描述</span><span class="sxs-lookup"><span data-stu-id="1d1d0-106">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="1d1d0-107">**SfcIsFileProtected**</span><span class="sxs-lookup"><span data-stu-id="1d1d0-107">**SfcIsFileProtected**</span></span>](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) | <span data-ttu-id="1d1d0-108">判斷指定的檔案是否受保護。</span><span class="sxs-lookup"><span data-stu-id="1d1d0-108">Determines whether the specified file is protected.</span></span>         |
| [<span data-ttu-id="1d1d0-109">**SfcIsKeyProtected**</span><span class="sxs-lookup"><span data-stu-id="1d1d0-109">**SfcIsKeyProtected**</span></span>](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)   | <span data-ttu-id="1d1d0-110">判斷指定的登錄機碼是否受到保護。</span><span class="sxs-lookup"><span data-stu-id="1d1d0-110">Determines whether the specified registry key is protected.</span></span> |



 

<span data-ttu-id="1d1d0-111">如果適用于作業系統，則應該使用此資料表中的函式，而不是已被取代的函式： [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) 和 [**SfcGetFiles**](sfcgetfiles.md)。</span><span class="sxs-lookup"><span data-stu-id="1d1d0-111">If available for the operating system, the functions in this table should be used rather than the deprecated functions: [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) and [**SfcGetFiles**](sfcgetfiles.md).</span></span>

 

 



