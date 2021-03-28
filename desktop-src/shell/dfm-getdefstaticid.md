---
description: 在建立期間由預設的內容功能表執行所傳送，指定預設的功能表命令，並允許進行替代選擇。 由 LPFNDFMCALLBACK 使用。
title: 'DFM_GETDEFSTATICID 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386115"
---
# <a name="dfm_getdefstaticid-message"></a><span data-ttu-id="41182-104">DFM \_ GETDEFSTATICID 訊息</span><span class="sxs-lookup"><span data-stu-id="41182-104">DFM\_GETDEFSTATICID message</span></span>

<span data-ttu-id="41182-105">在建立期間由預設的內容功能表執行所傳送，指定預設的功能表命令，並允許進行替代選擇。</span><span class="sxs-lookup"><span data-stu-id="41182-105">Sent by the default context menu implementation during creation, specifying the default menu command and allowing an alternate choice to be made.</span></span> <span data-ttu-id="41182-106">由 [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)使用。</span><span class="sxs-lookup"><span data-stu-id="41182-106">Used by [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span></span>


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a><span data-ttu-id="41182-107">參數</span><span class="sxs-lookup"><span data-stu-id="41182-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41182-108">*defaultID* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="41182-108">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41182-109">所選功能表命令的識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="41182-109">A pointer to the ID of the selected menu command.</span></span> <span data-ttu-id="41182-110">可辨識下列旗標。</span><span class="sxs-lookup"><span data-stu-id="41182-110">The following flag is recognized.</span></span>

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="41182-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM \_ CMD \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="41182-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="41182-112">顯示在其上叫用功能表之專案的 [ **屬性** ] UI。</span><span class="sxs-lookup"><span data-stu-id="41182-112">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41182-113">備註</span><span class="sxs-lookup"><span data-stu-id="41182-113">Remarks</span></span>

<span data-ttu-id="41182-114">若要覆寫預設的命令選擇，您的處理常式應該在收到此訊息時，將 *defaultID* 所指向的值設定為取代命令的識別碼，並傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="41182-114">To override the default command choice, your handler should, upon receipt of this message, set the value pointed to by *defaultID* to the ID of the replacement command and return S\_OK.</span></span> <span data-ttu-id="41182-115">傳回失敗碼，否則為。</span><span class="sxs-lookup"><span data-stu-id="41182-115">Return a failure code otherwise.</span></span>

<span data-ttu-id="41182-116">這則訊息會根據預設內容功能表物件的建立方式，傳送至回呼函式或回呼物件。</span><span class="sxs-lookup"><span data-stu-id="41182-116">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="41182-117">有兩個 Api 適用于其結構： [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="41182-117">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="41182-118">[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。</span><span class="sxs-lookup"><span data-stu-id="41182-118">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="41182-119">如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。</span><span class="sxs-lookup"><span data-stu-id="41182-119">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="41182-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="41182-120">Requirements</span></span>



| <span data-ttu-id="41182-121">需求</span><span class="sxs-lookup"><span data-stu-id="41182-121">Requirement</span></span> | <span data-ttu-id="41182-122">值</span><span class="sxs-lookup"><span data-stu-id="41182-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41182-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41182-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41182-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41182-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41182-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41182-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41182-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41182-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41182-127">標頭</span><span class="sxs-lookup"><span data-stu-id="41182-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="41182-128"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="41182-128"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
