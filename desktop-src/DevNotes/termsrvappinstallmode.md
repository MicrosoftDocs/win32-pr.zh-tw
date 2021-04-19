---
description: 判斷終端機伺服器是否處於安裝模式。
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: TermsrvAppInstallMode 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f80e51dc417cd637b2abaf8d5dfdc5c0d00f6578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981329"
---
# <a name="termsrvappinstallmode-function"></a><span data-ttu-id="7faf6-103">TermsrvAppInstallMode 函式</span><span class="sxs-lookup"><span data-stu-id="7faf6-103">TermsrvAppInstallMode function</span></span>

<span data-ttu-id="7faf6-104">\[這項功能不受支援，因此不應該使用。</span><span class="sxs-lookup"><span data-stu-id="7faf6-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="7faf6-105">它可能會在未事先通知的情況下，完全變更或消失。\]</span><span class="sxs-lookup"><span data-stu-id="7faf6-105">It may change or disappear completely without advance notice.\]</span></span>

<span data-ttu-id="7faf6-106">判斷終端機伺服器是否處於安裝模式。</span><span class="sxs-lookup"><span data-stu-id="7faf6-106">Determines whether the Terminal Server is in the INSTALL mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faf6-107">語法</span><span class="sxs-lookup"><span data-stu-id="7faf6-107">Syntax</span></span>


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a><span data-ttu-id="7faf6-108">參數</span><span class="sxs-lookup"><span data-stu-id="7faf6-108">Parameters</span></span>

<span data-ttu-id="7faf6-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="7faf6-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7faf6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7faf6-110">Return value</span></span>

<span data-ttu-id="7faf6-111">如果終端機伺服器處於安裝模式，則此函式會傳回 **TRUE** ，如果是在執行模式，則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7faf6-111">This function returns **TRUE** if the Terminal Server is in INSTALL mode and **FALSE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="7faf6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7faf6-112">Requirements</span></span>



| <span data-ttu-id="7faf6-113">需求</span><span class="sxs-lookup"><span data-stu-id="7faf6-113">Requirement</span></span> | <span data-ttu-id="7faf6-114">值</span><span class="sxs-lookup"><span data-stu-id="7faf6-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7faf6-115">DLL</span><span class="sxs-lookup"><span data-stu-id="7faf6-115">DLL</span></span><br/> | <dl> <span data-ttu-id="7faf6-116"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7faf6-116"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




