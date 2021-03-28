---
description: 由預設內容功能表程式傳送至要求 LPFNDFMCALLBACK，以叫用擴充的功能表命令。
title: 'DFM_INVOKECOMMANDEX 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dc96e9d0e4c27be8dee3ed7742874de4a3fb97e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511049"
---
# <a name="dfm_invokecommandex-message"></a><span data-ttu-id="48c1e-103">DFM \_ INVOKECOMMANDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="48c1e-103">DFM\_INVOKECOMMANDEX message</span></span>

<span data-ttu-id="48c1e-104">由預設內容功能表程式傳送至要求 [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) ，以叫用擴充的功能表命令。</span><span class="sxs-lookup"><span data-stu-id="48c1e-104">Sent by the default context menu implementation to request [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) to invoke an extended menu command.</span></span>


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a><span data-ttu-id="48c1e-105">參數</span><span class="sxs-lookup"><span data-stu-id="48c1e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c1e-106">*idCmd* \[\]</span><span class="sxs-lookup"><span data-stu-id="48c1e-106">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c1e-107">所選功能表命令的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="48c1e-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="48c1e-108">可辨識下列旗標。</span><span class="sxs-lookup"><span data-stu-id="48c1e-108">The following flags are recognized.</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="48c1e-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ CMD \_ DELETE**</span><span class="sxs-lookup"><span data-stu-id="48c1e-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="48c1e-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ CMD \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="48c1e-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="48c1e-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM \_ CMD \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="48c1e-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="48c1e-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ CMD \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="48c1e-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="48c1e-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM \_ CMD \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="48c1e-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="48c1e-114">顯示在其上叫用功能表之專案的 [ **屬性** ] UI。</span><span class="sxs-lookup"><span data-stu-id="48c1e-114">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="48c1e-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ CMD \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="48c1e-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="48c1e-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ CMD \_ 貼上**</span><span class="sxs-lookup"><span data-stu-id="48c1e-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="48c1e-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ CMD \_ VIEWLIST**</span><span class="sxs-lookup"><span data-stu-id="48c1e-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="48c1e-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ CMD \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="48c1e-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="48c1e-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ CMD \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="48c1e-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="48c1e-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ CMD \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="48c1e-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="48c1e-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ CMD \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="48c1e-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="48c1e-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ CMD \_ 重新命名**</span><span class="sxs-lookup"><span data-stu-id="48c1e-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="48c1e-123">*PDFMICS* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48c1e-123">*PDFMICS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c1e-124">[**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics)結構的指標，其中包含所選功能表命令的其他引數。</span><span class="sxs-lookup"><span data-stu-id="48c1e-124">A pointer to a [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) structure that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="48c1e-125">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="48c1e-125">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48c1e-126">備註</span><span class="sxs-lookup"><span data-stu-id="48c1e-126">Remarks</span></span>

<span data-ttu-id="48c1e-127">收到此訊息時， \_ 如果您想要讓預設的實值叫用命令的預設處理常式，則您的函式應傳回 S FALSE。</span><span class="sxs-lookup"><span data-stu-id="48c1e-127">Upon receipt of this message, your function should return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="48c1e-128">\_如果已處理訊息，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="48c1e-128">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="48c1e-129">否則，會傳回標準的 HRESULT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="48c1e-129">Otherwise, return a standard HRESULT error code.</span></span>

<span data-ttu-id="48c1e-130">這則訊息會根據回呼的實作為方式傳送至回呼函式或回呼物件。</span><span class="sxs-lookup"><span data-stu-id="48c1e-130">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="48c1e-131">有兩個 Api 可用於回呼結構、 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) ，其採用回呼函式的指標，或使用支援 [**ICoNtextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)的回呼物件的 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) 。</span><span class="sxs-lookup"><span data-stu-id="48c1e-131">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="48c1e-132">正在叫用命令的專案會在傳遞給回呼函式或 [**ICoNtextMenuCB：： callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) 方法的資料物件中提供。</span><span class="sxs-lookup"><span data-stu-id="48c1e-132">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="48c1e-133">這個資料物件是由執行回呼的資料來源所提供。</span><span class="sxs-lookup"><span data-stu-id="48c1e-133">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="48c1e-134">若要從資料物件中解壓縮專案，請使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)。</span><span class="sxs-lookup"><span data-stu-id="48c1e-134">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="48c1e-135">[**DFM \_INVOKECOMMAND**](dfm-invokecommand.md) 是此訊息較簡單的版本，不會提供太多的資訊給回呼。</span><span class="sxs-lookup"><span data-stu-id="48c1e-135">[**DFM\_INVOKECOMMAND**](dfm-invokecommand.md) is a simpler version of this message which does not provide as much information to the callback.</span></span> <span data-ttu-id="48c1e-136">如果您的執行不需要 **DFM \_ INVOKECOMMANDEX** 提供的額外資訊，請使用 **DFM \_ INVOKECOMMAND** 。</span><span class="sxs-lookup"><span data-stu-id="48c1e-136">Use **DFM\_INVOKECOMMAND** if the additional information provided by **DFM\_INVOKECOMMANDEX** is not needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c1e-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="48c1e-137">Requirements</span></span>



| <span data-ttu-id="48c1e-138">需求</span><span class="sxs-lookup"><span data-stu-id="48c1e-138">Requirement</span></span> | <span data-ttu-id="48c1e-139">值</span><span class="sxs-lookup"><span data-stu-id="48c1e-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48c1e-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48c1e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="48c1e-141">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48c1e-141">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="48c1e-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48c1e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="48c1e-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48c1e-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="48c1e-144">標頭</span><span class="sxs-lookup"><span data-stu-id="48c1e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="48c1e-145"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="48c1e-145"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
