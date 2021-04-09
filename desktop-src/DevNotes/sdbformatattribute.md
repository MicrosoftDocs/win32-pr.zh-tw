---
description: 將指定的屬性資料轉換為 XML 格式。
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: SdbFormatAttribute 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846900"
---
# <a name="sdbformatattribute-function"></a><span data-ttu-id="a70f7-103">SdbFormatAttribute 函式</span><span class="sxs-lookup"><span data-stu-id="a70f7-103">SdbFormatAttribute function</span></span>

<span data-ttu-id="a70f7-104">將指定的屬性資料轉換為 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="a70f7-104">Converts the specified attribute data to XML format.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="a70f7-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="a70f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="a70f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a70f7-107">*pAttrInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a70f7-107">*pAttrInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70f7-108">[**ATTRINFO**](attrinfo.md)結構。</span><span class="sxs-lookup"><span data-stu-id="a70f7-108">An [**ATTRINFO**](attrinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a70f7-109">*pchBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a70f7-109">*pchBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a70f7-110">輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a70f7-110">The output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a70f7-111">*dwBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a70f7-111">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70f7-112">*PchBuffer* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a70f7-112">The size of the *pchBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a70f7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a70f7-113">Return value</span></span>

<span data-ttu-id="a70f7-114">如果緩衝區太小，或找不到屬性，則函式會在成功時傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a70f7-114">The function returns **TRUE** on success or **FALSE** if the buffer is too small or the attribute is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="a70f7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a70f7-115">Requirements</span></span>



| <span data-ttu-id="a70f7-116">需求</span><span class="sxs-lookup"><span data-stu-id="a70f7-116">Requirement</span></span> | <span data-ttu-id="a70f7-117">值</span><span class="sxs-lookup"><span data-stu-id="a70f7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70f7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a70f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a70f7-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a70f7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a70f7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a70f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a70f7-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a70f7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a70f7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a70f7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a70f7-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a70f7-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a70f7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a70f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70f7-125">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="a70f7-125">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




