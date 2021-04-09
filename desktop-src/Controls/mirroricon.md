---
title: MirrorIcon 函式
description: 反轉 (鏡像) 圖示，使其在鏡像裝置內容上正確顯示。
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- MirrorIcon 函式 Windows 控制項
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024725"
---
# <a name="mirroricon-function"></a><span data-ttu-id="3a0ff-104">MirrorIcon 函式</span><span class="sxs-lookup"><span data-stu-id="3a0ff-104">MirrorIcon function</span></span>

<span data-ttu-id="3a0ff-105">\[**MirrorIcon** 可透過 Windows XP Service Pack 2 (SP2) 取得。</span><span class="sxs-lookup"><span data-stu-id="3a0ff-105">\[**MirrorIcon** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="3a0ff-106">它可能會在後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3a0ff-106">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="3a0ff-107">反轉 (鏡像) 圖示，使其在鏡像裝置內容上正確顯示。</span><span class="sxs-lookup"><span data-stu-id="3a0ff-107">Reverses (mirrors) icons so that they are displayed correctly on a mirrored device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0ff-108">語法</span><span class="sxs-lookup"><span data-stu-id="3a0ff-108">Syntax</span></span>


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a><span data-ttu-id="3a0ff-109">參數</span><span class="sxs-lookup"><span data-stu-id="3a0ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a0ff-110">*phIconSmall* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="3a0ff-110">*phIconSmall* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0ff-111">類型： \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="3a0ff-111">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="3a0ff-112">圖示控制碼的指標，該控制碼會參考小版本的圖示。</span><span class="sxs-lookup"><span data-stu-id="3a0ff-112">A pointer to the icon handle that references a small version of an icon.</span></span>

</dd> <dt>

<span data-ttu-id="3a0ff-113">_phIconLarge \* \[ in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="3a0ff-113">_phIconLarge\* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0ff-114">類型： \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="3a0ff-114">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="3a0ff-115">圖示控制碼的指標，參考大型版本的圖示。</span><span class="sxs-lookup"><span data-stu-id="3a0ff-115">A pointer to the icon handle that references a large version of an icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a0ff-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a0ff-116">Return value</span></span>

<span data-ttu-id="3a0ff-117">類型： _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span><span class="sxs-lookup"><span data-stu-id="3a0ff-117">Type: _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span></span>

<span data-ttu-id="3a0ff-118">如果成功，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3a0ff-118">**TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a0ff-119">備註</span><span class="sxs-lookup"><span data-stu-id="3a0ff-119">Remarks</span></span>

<span data-ttu-id="3a0ff-120">**MirrorIcon** 不會依名稱匯出，也不會在公用標頭檔中宣告。</span><span class="sxs-lookup"><span data-stu-id="3a0ff-120">**MirrorIcon** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="3a0ff-121">若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數414來取得函式指標。</span><span class="sxs-lookup"><span data-stu-id="3a0ff-121">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 414 from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a0ff-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a0ff-122">Requirements</span></span>



| <span data-ttu-id="3a0ff-123">需求</span><span class="sxs-lookup"><span data-stu-id="3a0ff-123">Requirement</span></span> | <span data-ttu-id="3a0ff-124">值</span><span class="sxs-lookup"><span data-stu-id="3a0ff-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0ff-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a0ff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a0ff-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a0ff-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="3a0ff-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a0ff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a0ff-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a0ff-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3a0ff-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3a0ff-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a0ff-130"><dt>Comctl32.dll (5.81 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3a0ff-130"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

