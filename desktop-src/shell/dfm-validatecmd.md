---
description: 傳送以確認功能表命令是否存在。
title: 'DFM_VALIDATECMD 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112337"
---
# <a name="dfm_validatecmd-message"></a><span data-ttu-id="1a0bd-103">DFM \_ VALIDATECMD 訊息</span><span class="sxs-lookup"><span data-stu-id="1a0bd-103">DFM\_VALIDATECMD message</span></span>

<span data-ttu-id="1a0bd-104">傳送以確認功能表命令是否存在。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-104">Sent to verify the existence of a menu command.</span></span>


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a><span data-ttu-id="1a0bd-105">參數</span><span class="sxs-lookup"><span data-stu-id="1a0bd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a0bd-106">*idCmd*</span><span class="sxs-lookup"><span data-stu-id="1a0bd-106">*idCmd*</span></span> 
</dt> <dd><span data-ttu-id="1a0bd-107">功能表命令識別碼位移。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-107">The menu command identifier offset.</span></span></dd> <dt>

<span data-ttu-id="1a0bd-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a0bd-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1a0bd-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-109">Not used.</span></span> <span data-ttu-id="1a0bd-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a0bd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a0bd-111">Return value</span></span>

<span data-ttu-id="1a0bd-112">\_如果命令存在，則傳回 s OK， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-112">Returns S\_OK if the command exists, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a0bd-113">備註</span><span class="sxs-lookup"><span data-stu-id="1a0bd-113">Remarks</span></span>

<span data-ttu-id="1a0bd-114">這則訊息會根據預設內容功能表物件的建立方式，傳送至回呼函式或回呼物件。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-114">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="1a0bd-115">有兩個 Api 適用于其結構： [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-115">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="1a0bd-116">[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-116">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="1a0bd-117">如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。</span><span class="sxs-lookup"><span data-stu-id="1a0bd-117">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a0bd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a0bd-118">Requirements</span></span>



| <span data-ttu-id="1a0bd-119">需求</span><span class="sxs-lookup"><span data-stu-id="1a0bd-119">Requirement</span></span> | <span data-ttu-id="1a0bd-120">值</span><span class="sxs-lookup"><span data-stu-id="1a0bd-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1a0bd-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a0bd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a0bd-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a0bd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1a0bd-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a0bd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a0bd-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a0bd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1a0bd-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1a0bd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a0bd-126"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a0bd-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




