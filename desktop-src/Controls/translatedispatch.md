---
title: TranslateDispatch 回呼函式
description: DoReaderMode 函式的用戶端使用它來攔截並明確處理以讀取器強制回應視窗的捲動區域為目標的任何 windows 訊息。 這是應用程式定義的回呼函數。
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- TranslateDispatch 回呼函式 Windows 控制項
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934265"
---
# <a name="translatedispatch-callback-function"></a><span data-ttu-id="1de5e-105">TranslateDispatch 回呼函式</span><span class="sxs-lookup"><span data-stu-id="1de5e-105">TranslateDispatch callback function</span></span>

<span data-ttu-id="1de5e-106">\[*TranslateDispatch* 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1de5e-106">\[*TranslateDispatch* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1de5e-107">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1de5e-107">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="1de5e-108">[**DoReaderMode**](doreadermode.md)函式的用戶端使用它來攔截並明確處理以讀取器強制回應視窗的捲動區域為目標的任何 windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="1de5e-108">Used by the client of the [**DoReaderMode**](doreadermode.md) function to intercept and explicitly handle any windows messages targeted for the scrolling area of the reader mode window.</span></span> <span data-ttu-id="1de5e-109">這是應用程式定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1de5e-109">This is an application-defined callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de5e-110">語法</span><span class="sxs-lookup"><span data-stu-id="1de5e-110">Syntax</span></span>


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a><span data-ttu-id="1de5e-111">參數</span><span class="sxs-lookup"><span data-stu-id="1de5e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1de5e-112">*lpmsg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1de5e-112">*lpmsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1de5e-113">類型： \**Const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \** _</span><span class="sxs-lookup"><span data-stu-id="1de5e-113">Type: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)\** _</span></span>

<span data-ttu-id="1de5e-114">_ 訊息結構的指標，其中包含攔截的訊息。 [ \*  ](/windows/win32/api/winuser/ns-winuser-msg)</span><span class="sxs-lookup"><span data-stu-id="1de5e-114">A pointer to an [_ *MSG*\*](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the intercepted message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1de5e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1de5e-115">Return value</span></span>

<span data-ttu-id="1de5e-116">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1de5e-116">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1de5e-117">如果此函式已處理訊息，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1de5e-117">**TRUE** if the message was handled by this function; otherwise, **FALSE**.</span></span> <span data-ttu-id="1de5e-118">如果 **為 FALSE**，則表示訊息是由預設讀取器模式執行所處理。</span><span class="sxs-lookup"><span data-stu-id="1de5e-118">If **FALSE**, the message is handled by the default reader mode implementation.</span></span> <span data-ttu-id="1de5e-119">該執行會處理滑鼠移動和按鈕，以及按鍵。</span><span class="sxs-lookup"><span data-stu-id="1de5e-119">That implementation handles mouse movement and buttons as well as key presses.</span></span>

## <a name="examples"></a><span data-ttu-id="1de5e-120">範例</span><span class="sxs-lookup"><span data-stu-id="1de5e-120">Examples</span></span>

<span data-ttu-id="1de5e-121">下列範例概述此函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="1de5e-121">The following example outlines an implementation of this function.</span></span>


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a><span data-ttu-id="1de5e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1de5e-122">Requirements</span></span>



| <span data-ttu-id="1de5e-123">需求</span><span class="sxs-lookup"><span data-stu-id="1de5e-123">Requirement</span></span> | <span data-ttu-id="1de5e-124">值</span><span class="sxs-lookup"><span data-stu-id="1de5e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1de5e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1de5e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1de5e-126">Windows Vista、Windows Vista \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1de5e-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1de5e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1de5e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1de5e-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1de5e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

