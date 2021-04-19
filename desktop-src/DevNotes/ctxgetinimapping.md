---
description: 判斷終端機伺服器是否僅在 Windows 終端機 Server 4.0) 上 (安裝模式。
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994840"
---
# <a name="ctxgetinimapping-function"></a><span data-ttu-id="69c85-103">CtxGetIniMapping 函式</span><span class="sxs-lookup"><span data-stu-id="69c85-103">CtxGetIniMapping function</span></span>

<span data-ttu-id="69c85-104">\[這項功能不受支援，因此不應該使用。</span><span class="sxs-lookup"><span data-stu-id="69c85-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="69c85-105">它可能會在未事先通知的情況下，完全變更或消失。</span><span class="sxs-lookup"><span data-stu-id="69c85-105">It may change or disappear completely without advance notice.</span></span> <span data-ttu-id="69c85-106">相反地，請使用 **VerifyVersionInfo**。\]</span><span class="sxs-lookup"><span data-stu-id="69c85-106">Instead, use **VerifyVersionInfo**.\]</span></span>

<span data-ttu-id="69c85-107">判斷終端機伺服器是否僅在 Windows 終端機 Server 4.0) 上 (安裝模式。</span><span class="sxs-lookup"><span data-stu-id="69c85-107">Determines whether the Terminal Server is in INSTALL mode (only on Windows Terminal Server 4.0).</span></span>

## <a name="syntax"></a><span data-ttu-id="69c85-108">語法</span><span class="sxs-lookup"><span data-stu-id="69c85-108">Syntax</span></span>


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a><span data-ttu-id="69c85-109">參數</span><span class="sxs-lookup"><span data-stu-id="69c85-109">Parameters</span></span>

<span data-ttu-id="69c85-110">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="69c85-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69c85-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="69c85-111">Return value</span></span>

<span data-ttu-id="69c85-112">如果終端機伺服器處於 [安裝] 模式，則此函式會傳回 **FALSE** ，如果是在執行模式， **則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="69c85-112">This function returns **FALSE** if the Terminal Server is in INSTALL mode, **TRUE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c85-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="69c85-113">Requirements</span></span>



| <span data-ttu-id="69c85-114">需求</span><span class="sxs-lookup"><span data-stu-id="69c85-114">Requirement</span></span> | <span data-ttu-id="69c85-115">值</span><span class="sxs-lookup"><span data-stu-id="69c85-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69c85-116">DLL</span><span class="sxs-lookup"><span data-stu-id="69c85-116">DLL</span></span><br/> | <dl> <span data-ttu-id="69c85-117"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69c85-117"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c85-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69c85-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c85-119">**VerifyVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="69c85-119">**VerifyVersionInfo**</span></span>](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
