---
description: 取得符合所指定雜湊的雜湊識別規則層級。
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468409"
---
# <a name="saferisearchmatchinghashrules-function"></a><span data-ttu-id="63312-103">SaferiSearchMatchingHashRules 函式</span><span class="sxs-lookup"><span data-stu-id="63312-103">SaferiSearchMatchingHashRules function</span></span>

<span data-ttu-id="63312-104">取得符合所指定雜湊的雜湊識別規則層級。</span><span class="sxs-lookup"><span data-stu-id="63312-104">Gets the level of a hash identification rule that matches the specified hash.</span></span>

<span data-ttu-id="63312-105">此函數沒有相關聯的匯入程式庫，而且未在公用標頭中宣告。</span><span class="sxs-lookup"><span data-stu-id="63312-105">This function has no associated import library and is not declared in a public header.</span></span> <span data-ttu-id="63312-106">您必須使用這個函式的簽章來定義函式指標，而且您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以動態方式連結至 Advapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="63312-106">You must define a function pointer with the signature of this function, and you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

<span data-ttu-id="63312-107">我們建議使用 [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) 函式來評估軟體限制原則。</span><span class="sxs-lookup"><span data-stu-id="63312-107">We recommend using the [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) function to evaluate software restriction policies.</span></span>

## <a name="syntax"></a><span data-ttu-id="63312-108">語法</span><span class="sxs-lookup"><span data-stu-id="63312-108">Syntax</span></span>


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a><span data-ttu-id="63312-109">參數</span><span class="sxs-lookup"><span data-stu-id="63312-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63312-110">*HashAlgorithm* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="63312-110">*HashAlgorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63312-111">用來建立雜湊之演算法的識別碼。</span><span class="sxs-lookup"><span data-stu-id="63312-111">The identifier of the algorithm used to create the hash.</span></span>

</dd> <dt>

<span data-ttu-id="63312-112">*pHashBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63312-112">*pHashBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63312-113">包含雜湊的位元組陣列指標。</span><span class="sxs-lookup"><span data-stu-id="63312-113">A pointer to an array of bytes that contains the hash.</span></span>

</dd> <dt>

<span data-ttu-id="63312-114">*dwHashSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63312-114">*dwHashSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63312-115">*PHashBytes* 陣列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="63312-115">The size, in bytes, of the *pHashBytes* array.</span></span>

</dd> <dt>

<span data-ttu-id="63312-116">*dwOriginalImageSize* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="63312-116">*dwOriginalImageSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63312-117">計算雜湊之原始影像的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="63312-117">The size, in bytes, of the original image from which the hash was computed.</span></span>

</dd> <dt>

<span data-ttu-id="63312-118">*pdwFoundLevel* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="63312-118">*pdwFoundLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63312-119">符合雜湊識別碼規則之層級識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="63312-119">A pointer to the level identifier for the matching hash identification rule.</span></span>

</dd> <dt>

<span data-ttu-id="63312-120">*pdwSaferFlags*</span><span class="sxs-lookup"><span data-stu-id="63312-120">*pdwSaferFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="63312-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="63312-121">Reserved.</span></span> <span data-ttu-id="63312-122">將此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="63312-122">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63312-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="63312-123">Return value</span></span>

<span data-ttu-id="63312-124">如果函式成功，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="63312-124">**TRUE** if the function is successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="63312-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="63312-125">Requirements</span></span>



| <span data-ttu-id="63312-126">需求</span><span class="sxs-lookup"><span data-stu-id="63312-126">Requirement</span></span> | <span data-ttu-id="63312-127">值</span><span class="sxs-lookup"><span data-stu-id="63312-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63312-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63312-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63312-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63312-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="63312-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63312-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63312-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63312-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63312-132">DLL</span><span class="sxs-lookup"><span data-stu-id="63312-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63312-133"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63312-133"><dt>Advapi32.dll</dt></span></span> </dl> |



 

 
