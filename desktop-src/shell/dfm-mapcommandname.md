---
description: 由預設內容功能表執行所傳送，以將名稱指派給功能表命令。
title: 'DFM_MAPCOMMANDNAME 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511048"
---
# <a name="dfm_mapcommandname-message"></a><span data-ttu-id="86760-103">DFM \_ MAPCOMMANDNAME 訊息</span><span class="sxs-lookup"><span data-stu-id="86760-103">DFM\_MAPCOMMANDNAME message</span></span>

<span data-ttu-id="86760-104">由預設內容功能表執行所傳送，以將名稱指派給功能表命令。</span><span class="sxs-lookup"><span data-stu-id="86760-104">Sent by the default context menu implementation to assign a name to a menu command.</span></span>


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a><span data-ttu-id="86760-105">參數</span><span class="sxs-lookup"><span data-stu-id="86760-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86760-106">*defaultID* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="86760-106">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86760-107">所選功能表命令的識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="86760-107">A pointer to the ID of the selected menu command.</span></span>

</dd> <dt>

<span data-ttu-id="86760-108">*pszCommandName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86760-108">*pszCommandName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86760-109">Unicode 字串的指標，其中包含命令的名稱。</span><span class="sxs-lookup"><span data-stu-id="86760-109">A pointer to a Unicode string containing the name of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86760-110">備註</span><span class="sxs-lookup"><span data-stu-id="86760-110">Remarks</span></span>

<span data-ttu-id="86760-111">這則訊息會傳送至回呼函式或回呼物件（根據預設的內容功能表物件的執行方式而定）。</span><span class="sxs-lookup"><span data-stu-id="86760-111">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="86760-112">有兩個 Api 適用于其實 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="86760-112">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="86760-113">[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。</span><span class="sxs-lookup"><span data-stu-id="86760-113">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="86760-114">如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。</span><span class="sxs-lookup"><span data-stu-id="86760-114">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="86760-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="86760-115">Requirements</span></span>



| <span data-ttu-id="86760-116">需求</span><span class="sxs-lookup"><span data-stu-id="86760-116">Requirement</span></span> | <span data-ttu-id="86760-117">值</span><span class="sxs-lookup"><span data-stu-id="86760-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="86760-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86760-118">Minimum supported client</span></span><br/> | <span data-ttu-id="86760-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86760-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="86760-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86760-120">Minimum supported server</span></span><br/> | <span data-ttu-id="86760-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86760-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="86760-122">標頭</span><span class="sxs-lookup"><span data-stu-id="86760-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="86760-123"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="86760-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




