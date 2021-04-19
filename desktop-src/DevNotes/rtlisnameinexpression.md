---
description: 判斷 Unicode 字串是否符合指定的模式。
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972126"
---
# <a name="rtlisnameinexpression-function"></a><span data-ttu-id="370dc-103">RtlIsNameInExpression 函式</span><span class="sxs-lookup"><span data-stu-id="370dc-103">RtlIsNameInExpression function</span></span>

<span data-ttu-id="370dc-104">判斷 Unicode 字串是否符合指定的模式。</span><span class="sxs-lookup"><span data-stu-id="370dc-104">Determines whether a Unicode string matches the specified pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="370dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="370dc-105">Syntax</span></span>


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a><span data-ttu-id="370dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="370dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="370dc-107">*運算式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="370dc-107">*Expression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="370dc-108">模式字串的指標。</span><span class="sxs-lookup"><span data-stu-id="370dc-108">A pointer to the pattern string.</span></span> <span data-ttu-id="370dc-109">這個字串可以包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="370dc-109">This string can contain wildcard characters.</span></span> <span data-ttu-id="370dc-110">如果 *IgnoreCase* 參數為 TRUE，則字串必須只包含大寫字元。</span><span class="sxs-lookup"><span data-stu-id="370dc-110">If the *IgnoreCase* parameter is TRUE, the string must contain only uppercase characters.</span></span>

</dd> <dt>

<span data-ttu-id="370dc-111">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="370dc-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="370dc-112">要與模式比較之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="370dc-112">A pointer to the string to be compared against the pattern.</span></span> <span data-ttu-id="370dc-113">這個字串不能包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="370dc-113">This string cannot contain wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="370dc-114">*IgnoreCase* \[在\]</span><span class="sxs-lookup"><span data-stu-id="370dc-114">*IgnoreCase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="370dc-115">**如果** 不區分大小寫比對，則為 TRUE，如果區分大小寫比對，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="370dc-115">**TRUE** for case-insensitive matching, or **FALSE** for case-sensitive matching.</span></span>

</dd> <dt>

<span data-ttu-id="370dc-116">*UpcaseTable* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="370dc-116">*UpcaseTable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="370dc-117">大寫字元資料表的選擇性指標，用於不區分大小寫比對。</span><span class="sxs-lookup"><span data-stu-id="370dc-117">An optional pointer to an uppercase character table to use for case-insensitive matching.</span></span> <span data-ttu-id="370dc-118">如果此參數為 Null，則會使用預設系統大寫字元資料表。</span><span class="sxs-lookup"><span data-stu-id="370dc-118">If this parameter is NULL, the default system uppercase character table is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="370dc-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="370dc-119">Return value</span></span>

<span data-ttu-id="370dc-120">如果字串符合模式，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="370dc-120">Returns **TRUE** if the string matches the pattern.</span></span> <span data-ttu-id="370dc-121">如果字串不符合模式，則此函式會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="370dc-121">If the string does not match the pattern, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="370dc-122">備註</span><span class="sxs-lookup"><span data-stu-id="370dc-122">Remarks</span></span>

<span data-ttu-id="370dc-123">此函數沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="370dc-123">This function has no associated header file.</span></span> <span data-ttu-id="370dc-124">相關聯的匯入程式庫（Ntdll.dll）可在 Microsoft Windows 驅動程式套件 (WDK) 中取得。</span><span class="sxs-lookup"><span data-stu-id="370dc-124">The associated import library, Ntdll.lib, is available in the Microsoft Windows Driver Kit (WDK).</span></span> <span data-ttu-id="370dc-125">您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式來呼叫這個函式，以動態連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="370dc-125">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="370dc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="370dc-126">Requirements</span></span>



| <span data-ttu-id="370dc-127">需求</span><span class="sxs-lookup"><span data-stu-id="370dc-127">Requirement</span></span> | <span data-ttu-id="370dc-128">值</span><span class="sxs-lookup"><span data-stu-id="370dc-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="370dc-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="370dc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="370dc-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="370dc-130">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="370dc-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="370dc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="370dc-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="370dc-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="370dc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="370dc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="370dc-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="370dc-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
