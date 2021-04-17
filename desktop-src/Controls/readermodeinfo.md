---
title: READERMODEINFO 結構
description: 包含初始化 DoReaderMode 函數所需的資訊。
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- READERMODEINFO 結構 Windows 控制項
- PREADERMODEINFO 結構指標視窗控制項
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466065"
---
# <a name="readermodeinfo-structure"></a><span data-ttu-id="e836d-105">READERMODEINFO 結構</span><span class="sxs-lookup"><span data-stu-id="e836d-105">READERMODEINFO structure</span></span>

<span data-ttu-id="e836d-106">\[**READERMODEINFO** 可透過 Windows XP Service Pack 2 (SP2) 來支援。</span><span class="sxs-lookup"><span data-stu-id="e836d-106">\[**READERMODEINFO** is supported through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="e836d-107">可能在後續版本中不支援。\]</span><span class="sxs-lookup"><span data-stu-id="e836d-107">It might be unsupported in subsequent versions.\]</span></span>

<span data-ttu-id="e836d-108">包含初始化 [**DoReaderMode**](doreadermode.md) 函數所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="e836d-108">Contains information required to initialize the [**DoReaderMode**](doreadermode.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e836d-109">語法</span><span class="sxs-lookup"><span data-stu-id="e836d-109">Syntax</span></span>


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a><span data-ttu-id="e836d-110">成員</span><span class="sxs-lookup"><span data-stu-id="e836d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e836d-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="e836d-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e836d-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e836d-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e836d-113">必要。</span><span class="sxs-lookup"><span data-stu-id="e836d-113">Required.</span></span> <span data-ttu-id="e836d-114">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e836d-114">The size of the structure, in bytes.</span></span> <span data-ttu-id="e836d-115">在呼叫 [**DoReaderMode**](doreadermode.md)之前，請將此參數設定為 **sizeof (READERMODE)** 。</span><span class="sxs-lookup"><span data-stu-id="e836d-115">Set this parameter to **sizeof(READERMODE)** before you call [**DoReaderMode**](doreadermode.md).</span></span>

</dd> <dt>

<span data-ttu-id="e836d-116">**hwnd**</span><span class="sxs-lookup"><span data-stu-id="e836d-116">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="e836d-117">類型： **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e836d-117">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e836d-118">必要。</span><span class="sxs-lookup"><span data-stu-id="e836d-118">Required.</span></span> <span data-ttu-id="e836d-119">要用於讀取器模式的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="e836d-119">The handle of the window to be used for reader mode.</span></span>

</dd> <dt>

<span data-ttu-id="e836d-120">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="e836d-120">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e836d-121">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e836d-121">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e836d-122">旗標：自訂讀取器強制回應視窗的功能。</span><span class="sxs-lookup"><span data-stu-id="e836d-122">Flags customizing the functionality of the reader mode window.</span></span> <span data-ttu-id="e836d-123">此參數可以是 0;否則為下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="e836d-123">This parameter can be 0; otherwise, one or more of the following values.</span></span>



| <span data-ttu-id="e836d-124">值</span><span class="sxs-lookup"><span data-stu-id="e836d-124">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="e836d-125">意義</span><span class="sxs-lookup"><span data-stu-id="e836d-125">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <span data-ttu-id="e836d-126"><dt>**RMF \_ZEROCURSOR**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e836d-126"><dt>**RMF\_ZEROCURSOR**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="e836d-127">將游標放在位於 **prc** 指定區域的中央。</span><span class="sxs-lookup"><span data-stu-id="e836d-127">Sets the cursor in the center of the area specified in **prc**.</span></span> <span data-ttu-id="e836d-128">如果未指定此旗標，資料指標位置會維持不變。</span><span class="sxs-lookup"><span data-stu-id="e836d-128">If this flag is not specified, the cursor position remains unchanged.</span></span><br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <span data-ttu-id="e836d-129"><dt>**RMF \_VERTICALONLY**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e836d-129"><dt>**RMF\_VERTICALONLY**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="e836d-130">只允許垂直捲動。</span><span class="sxs-lookup"><span data-stu-id="e836d-130">Allows only vertical scrolling.</span></span><br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <span data-ttu-id="e836d-131"><dt>**RMF \_HORIZONTALONLY**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="e836d-131"><dt>**RMF\_HORIZONTALONLY**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="e836d-132">只允許水準滾動。</span><span class="sxs-lookup"><span data-stu-id="e836d-132">Allows only horizontal scrolling.</span></span><br/>                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="e836d-133">**中國**</span><span class="sxs-lookup"><span data-stu-id="e836d-133">**prc**</span></span>
</dt> <dd>

<span data-ttu-id="e836d-134">類型： **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="e836d-134">Type: **LPRECT**</span></span>

</dd> <dd>

<span data-ttu-id="e836d-135">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會指定讀取器強制回應視窗中的捲動區域。</span><span class="sxs-lookup"><span data-stu-id="e836d-135">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the scrolling area in the reader mode window.</span></span> <span data-ttu-id="e836d-136">如果這個成員是 **Null**，則會將整個視窗當做捲動區域使用。</span><span class="sxs-lookup"><span data-stu-id="e836d-136">If this member is **NULL**, then the entire window is used as the scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="e836d-137">**pfnScroll**</span><span class="sxs-lookup"><span data-stu-id="e836d-137">**pfnScroll**</span></span>
</dt> <dd>

<span data-ttu-id="e836d-138">類型： **PFNREADERSCROLL**</span><span class="sxs-lookup"><span data-stu-id="e836d-138">Type: **PFNREADERSCROLL**</span></span>

</dd> <dd>

<span data-ttu-id="e836d-139">應用程式定義的 [*ReaderScroll*](readerscroll.md) 回呼函式的指標，用來通知應用程式視窗需要以特定方向進行滾動。</span><span class="sxs-lookup"><span data-stu-id="e836d-139">A pointer to an application-defined [*ReaderScroll*](readerscroll.md) callback function used to notify the application that the window needs to be scrolled in a particular direction.</span></span>

</dd> <dt>

<span data-ttu-id="e836d-140">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="e836d-140">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e836d-141">類型： **PFNREADERTRANSLATEDISPATCH**</span><span class="sxs-lookup"><span data-stu-id="e836d-141">Type: **PFNREADERTRANSLATEDISPATCH**</span></span>

</dd> <dd>

<span data-ttu-id="e836d-142">應用程式定義的 [*TranslateDispatch*](translatedispatch.md) 回呼函式的指標，用來取得傳送至讀取器強制回應視窗之任何訊息的第一個通知。</span><span class="sxs-lookup"><span data-stu-id="e836d-142">A pointer to an application-defined [*TranslateDispatch*](translatedispatch.md) callback function used to get first notification of any messages sent to the reader mode window.</span></span>

</dd> <dt>

<span data-ttu-id="e836d-143">**lParam**</span><span class="sxs-lookup"><span data-stu-id="e836d-143">**lParam**</span></span>
</dt> <dd>

<span data-ttu-id="e836d-144">類型： **[ **LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e836d-144">Type: **[**LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e836d-145">應用程式所需的其他資訊，由呼叫端在 [*ReaderScroll*](readerscroll.md) 回呼函數中讀取。</span><span class="sxs-lookup"><span data-stu-id="e836d-145">Additional information as needed by the application, read by the caller in the [*ReaderScroll*](readerscroll.md) callback function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e836d-146">備註</span><span class="sxs-lookup"><span data-stu-id="e836d-146">Remarks</span></span>

<span data-ttu-id="e836d-147">未在任何公用標頭中宣告此結構。</span><span class="sxs-lookup"><span data-stu-id="e836d-147">This structure is not declared in any public header.</span></span> <span data-ttu-id="e836d-148">若要使用它，您必須在自己的標頭中包含如上所示的宣告。</span><span class="sxs-lookup"><span data-stu-id="e836d-148">To use it, you must include the declaration shown above in your own header.</span></span>

## <a name="requirements"></a><span data-ttu-id="e836d-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="e836d-149">Requirements</span></span>



| <span data-ttu-id="e836d-150">需求</span><span class="sxs-lookup"><span data-stu-id="e836d-150">Requirement</span></span> | <span data-ttu-id="e836d-151">值</span><span class="sxs-lookup"><span data-stu-id="e836d-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e836d-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e836d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e836d-153">Windows Vista、Windows Vista \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e836d-153">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e836d-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e836d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e836d-155">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e836d-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

