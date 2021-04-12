---
description: 抓取指定檔案的屬性資料。
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109917"
---
# <a name="sdbgetfileattributes-function"></a><span data-ttu-id="28da0-103">SdbGetFileAttributes 函式</span><span class="sxs-lookup"><span data-stu-id="28da0-103">SdbGetFileAttributes function</span></span>

<span data-ttu-id="28da0-104">抓取指定檔案的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="28da0-104">Retrieves the attribute data for the specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="28da0-105">語法</span><span class="sxs-lookup"><span data-stu-id="28da0-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a><span data-ttu-id="28da0-106">參數</span><span class="sxs-lookup"><span data-stu-id="28da0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28da0-107">*lpwszFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28da0-107">*lpwszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28da0-108">檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="28da0-108">The path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="28da0-109">*ppAttrInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28da0-109">*ppAttrInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28da0-110">[**ATTRINFO**](attrinfo.md)結構的陣列，其中包含屬性資料。</span><span class="sxs-lookup"><span data-stu-id="28da0-110">An array of [**ATTRINFO**](attrinfo.md) structures that contain the attribute data.</span></span>

</dd> <dt>

<span data-ttu-id="28da0-111">*lpdwAttrCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28da0-111">*lpdwAttrCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28da0-112">屬性的數目。</span><span class="sxs-lookup"><span data-stu-id="28da0-112">The number of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28da0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="28da0-113">Return value</span></span>

<span data-ttu-id="28da0-114">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="28da0-114">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="28da0-115">備註</span><span class="sxs-lookup"><span data-stu-id="28da0-115">Remarks</span></span>

<span data-ttu-id="28da0-116">當您完成資料時，請使用 [**SdbFreeFileAttributes**](sdbfreefileattributes.md) 函數釋出資料。</span><span class="sxs-lookup"><span data-stu-id="28da0-116">When you have finished with the data, free it using the [**SdbFreeFileAttributes**](sdbfreefileattributes.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28da0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="28da0-117">Requirements</span></span>



| <span data-ttu-id="28da0-118">需求</span><span class="sxs-lookup"><span data-stu-id="28da0-118">Requirement</span></span> | <span data-ttu-id="28da0-119">值</span><span class="sxs-lookup"><span data-stu-id="28da0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28da0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28da0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28da0-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28da0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="28da0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28da0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28da0-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28da0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="28da0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="28da0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28da0-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28da0-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28da0-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28da0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28da0-127">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="28da0-127">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="28da0-128">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="28da0-128">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> </dl>

 

 




