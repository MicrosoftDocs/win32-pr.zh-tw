---
description: 捕獲系統 AppPatch 目錄。
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109924"
---
# <a name="sdbgetapppatchdir-function"></a><span data-ttu-id="2c51c-103">SdbGetAppPatchDir 函式</span><span class="sxs-lookup"><span data-stu-id="2c51c-103">SdbGetAppPatchDir function</span></span>

<span data-ttu-id="2c51c-104">捕獲系統 AppPatch 目錄。</span><span class="sxs-lookup"><span data-stu-id="2c51c-104">Retrieves the system AppPatch directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c51c-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c51c-105">Syntax</span></span>


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a><span data-ttu-id="2c51c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c51c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c51c-107">*hSDB* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2c51c-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c51c-108">[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2c51c-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2c51c-109">*szAppPatchPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2c51c-109">*szAppPatchPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c51c-110">產生的路徑。</span><span class="sxs-lookup"><span data-stu-id="2c51c-110">The resulting path.</span></span>

</dd> <dt>

<span data-ttu-id="2c51c-111">*cchSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c51c-111">*cchSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c51c-112">*SzAppPatchPath* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2c51c-112">The size of the *szAppPatchPath* buffer, in characters.</span></span> <span data-ttu-id="2c51c-113">如果函式失敗，這個參數會設為空字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="2c51c-113">If the function fails, this parameter is set to the empty string ("").</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c51c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c51c-114">Return value</span></span>

<span data-ttu-id="2c51c-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c51c-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c51c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c51c-116">Requirements</span></span>



| <span data-ttu-id="2c51c-117">需求</span><span class="sxs-lookup"><span data-stu-id="2c51c-117">Requirement</span></span> | <span data-ttu-id="2c51c-118">值</span><span class="sxs-lookup"><span data-stu-id="2c51c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c51c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c51c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c51c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c51c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2c51c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c51c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c51c-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c51c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2c51c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2c51c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c51c-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c51c-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c51c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c51c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c51c-126">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="2c51c-126">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




