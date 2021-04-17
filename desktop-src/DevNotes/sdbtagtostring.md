---
description: 抓取指定標記的顯示名稱。
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468148"
---
# <a name="sdbtagtostring-function"></a><span data-ttu-id="4b04a-103">SdbTagToString 函式</span><span class="sxs-lookup"><span data-stu-id="4b04a-103">SdbTagToString function</span></span>

<span data-ttu-id="4b04a-104">抓取指定標記的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4b04a-104">Retrieves the display name of the specified TAG.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b04a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4b04a-105">Syntax</span></span>


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a><span data-ttu-id="4b04a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4b04a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b04a-107">*標記* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b04a-107">*tag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b04a-108">標記。</span><span class="sxs-lookup"><span data-stu-id="4b04a-108">The TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b04a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b04a-109">Return value</span></span>

<span data-ttu-id="4b04a-110">函數會傳回以 null 結束的字串或 "InvalidTag" 的指標。</span><span class="sxs-lookup"><span data-stu-id="4b04a-110">The function returns a pointer to the null-terminated string or "InvalidTag".</span></span>

## <a name="requirements"></a><span data-ttu-id="4b04a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b04a-111">Requirements</span></span>



| <span data-ttu-id="4b04a-112">需求</span><span class="sxs-lookup"><span data-stu-id="4b04a-112">Requirement</span></span> | <span data-ttu-id="4b04a-113">值</span><span class="sxs-lookup"><span data-stu-id="4b04a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b04a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b04a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4b04a-115">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b04a-115">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4b04a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b04a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4b04a-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b04a-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4b04a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="4b04a-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b04a-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b04a-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b04a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b04a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b04a-121">**標記**</span><span class="sxs-lookup"><span data-stu-id="4b04a-121">**TAG**</span></span>](tag.md)
</dt> </dl>

 

 




