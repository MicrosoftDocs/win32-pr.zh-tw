---
description: 由預設內容功能表的執行所傳送，以要求處理功能表 (LPFNDFMCALLBACK) 叫用功能表命令的回呼函數。
title: 'DFM_INVOKECOMMAND 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd3200a6-b9e7-414c-9a01-c432cb306dba
api_name:
- DFM_INVOKECOMMAND
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 168b25833deb6bde2424ea4552f4600b83bc9679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972017"
---
# <a name="dfm_invokecommand-message"></a><span data-ttu-id="caa70-103">DFM \_ INVOKECOMMAND 訊息</span><span class="sxs-lookup"><span data-stu-id="caa70-103">DFM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="caa70-104">由預設內容功能表的執行所傳送，以要求處理功能表 ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) 叫用功能表命令的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="caa70-104">Sent by the default context menu implementation to request the callback function that handles the menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) to invoke a menu command.</span></span>


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a><span data-ttu-id="caa70-105">參數</span><span class="sxs-lookup"><span data-stu-id="caa70-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caa70-106"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="caa70-106">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caa70-107">所選功能表命令的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="caa70-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="caa70-108">可辨識下列旗標：</span><span class="sxs-lookup"><span data-stu-id="caa70-108">The following flags are recognized:</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="caa70-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ CMD \_ DELETE**</span><span class="sxs-lookup"><span data-stu-id="caa70-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-110">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="caa70-110">**Windows Vista and later**.</span></span> <span data-ttu-id="caa70-111">刪除目前的專案。</span><span class="sxs-lookup"><span data-stu-id="caa70-111">Delete the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="caa70-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ CMD \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="caa70-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-113">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="caa70-113">**Windows Vista and later**.</span></span> <span data-ttu-id="caa70-114">移動目前的專案。</span><span class="sxs-lookup"><span data-stu-id="caa70-114">Move the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="caa70-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM \_ CMD \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="caa70-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-116">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="caa70-116">**Windows Vista and later**.</span></span> <span data-ttu-id="caa70-117">複製目前的專案。</span><span class="sxs-lookup"><span data-stu-id="caa70-117">Copy the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="caa70-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ CMD \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="caa70-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-119">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="caa70-119">**Windows Vista and later**.</span></span> <span data-ttu-id="caa70-120">建立目前專案的連結。</span><span class="sxs-lookup"><span data-stu-id="caa70-120">Create a link to the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="caa70-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM \_ CMD \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="caa70-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-122">針對叫用功能表的專案顯示 [ **屬性** ] UI。</span><span class="sxs-lookup"><span data-stu-id="caa70-122">Show the **Properties** UI for the item on which the menu was invoked.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="caa70-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ CMD \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="caa70-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-124">不支援。</span><span class="sxs-lookup"><span data-stu-id="caa70-124">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="caa70-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ CMD \_ 貼上**</span><span class="sxs-lookup"><span data-stu-id="caa70-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-126">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="caa70-126">**Windows Vista and later**.</span></span> <span data-ttu-id="caa70-127">將專案貼到目前的位置。</span><span class="sxs-lookup"><span data-stu-id="caa70-127">Paste an item to the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="caa70-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ CMD \_ VIEWLIST**</span><span class="sxs-lookup"><span data-stu-id="caa70-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-129">不支援。</span><span class="sxs-lookup"><span data-stu-id="caa70-129">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="caa70-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ CMD \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="caa70-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-131">不支援。</span><span class="sxs-lookup"><span data-stu-id="caa70-131">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="caa70-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ CMD \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="caa70-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-133">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="caa70-133">**Windows Vista and later**.</span></span> <span data-ttu-id="caa70-134">將連結貼到目前的位置。</span><span class="sxs-lookup"><span data-stu-id="caa70-134">Paste a link at the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="caa70-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ CMD \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="caa70-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-136">不支援。</span><span class="sxs-lookup"><span data-stu-id="caa70-136">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="caa70-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ CMD \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="caa70-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-138">不支援。</span><span class="sxs-lookup"><span data-stu-id="caa70-138">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="caa70-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ CMD \_ 重新命名**</span><span class="sxs-lookup"><span data-stu-id="caa70-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd>

<span data-ttu-id="caa70-140">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="caa70-140">**Windows Vista and later**.</span></span> <span data-ttu-id="caa70-141">重新命名目前的專案。</span><span class="sxs-lookup"><span data-stu-id="caa70-141">Rename the current item.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="caa70-142">*args* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caa70-142">*args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caa70-143">以 null 結束的字串指標，其中包含所選功能表命令的其他引數。</span><span class="sxs-lookup"><span data-stu-id="caa70-143">A pointer to a null-terminated string that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="caa70-144">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="caa70-144">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caa70-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="caa70-145">Return value</span></span>

<span data-ttu-id="caa70-146">\_如果您希望預設的實值叫用命令的預設處理常式，則此訊息的處理常式必須傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="caa70-146">The handler for this message needs to return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="caa70-147">\_如果已處理訊息，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="caa70-147">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="caa70-148">否則，會傳回標準的 HRESULT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="caa70-148">Otherwise, return a standard HRESULT error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa70-149">備註</span><span class="sxs-lookup"><span data-stu-id="caa70-149">Remarks</span></span>

<span data-ttu-id="caa70-150">這則訊息會根據回呼的實作為方式傳送至回呼函式或回呼物件。</span><span class="sxs-lookup"><span data-stu-id="caa70-150">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="caa70-151">有兩個 Api 可用於回呼結構、 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) ，其採用回呼函式的指標，或使用支援 [**ICoNtextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)的回呼物件的 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) 。</span><span class="sxs-lookup"><span data-stu-id="caa70-151">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="caa70-152">正在叫用命令的專案會在傳遞給回呼函式或 [**ICoNtextMenuCB：： callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) 方法的資料物件中提供。</span><span class="sxs-lookup"><span data-stu-id="caa70-152">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="caa70-153">這個資料物件是由執行回呼的資料來源所提供。</span><span class="sxs-lookup"><span data-stu-id="caa70-153">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="caa70-154">若要從資料物件中解壓縮專案，請使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)。</span><span class="sxs-lookup"><span data-stu-id="caa70-154">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="caa70-155">[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。</span><span class="sxs-lookup"><span data-stu-id="caa70-155">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="caa70-156">如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。</span><span class="sxs-lookup"><span data-stu-id="caa70-156">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="caa70-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="caa70-157">Requirements</span></span>



| <span data-ttu-id="caa70-158">需求</span><span class="sxs-lookup"><span data-stu-id="caa70-158">Requirement</span></span> | <span data-ttu-id="caa70-159">值</span><span class="sxs-lookup"><span data-stu-id="caa70-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="caa70-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caa70-160">Minimum supported client</span></span><br/> | <span data-ttu-id="caa70-161">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caa70-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="caa70-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caa70-162">Minimum supported server</span></span><br/> | <span data-ttu-id="caa70-163">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caa70-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="caa70-164">標頭</span><span class="sxs-lookup"><span data-stu-id="caa70-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa70-165"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="caa70-165"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
