---
title: 'CFSTR_DSOP_DS_SELECTION_LIST (Objsel) '
description: CFSTR \_ DSOP \_ ds \_ 選擇 \_ 清單剪貼簿格式會提供包含 DS \_ 選擇 \_ 清單結構的 HGLOBAL。 DS \_ 選擇 \_ 清單結構包含在目錄物件選擇器對話方塊中選取之專案的相關資料。
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934215"
---
# <a name="cfstr_dsop_ds_selection_list"></a><span data-ttu-id="558f6-104">CFSTR \_ DSOP \_ DS \_ 選擇 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="558f6-104">CFSTR\_DSOP\_DS\_SELECTION\_LIST</span></span>

<dl> <dt>

<span data-ttu-id="558f6-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR \_ DSOP \_ DS \_ 選擇 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="558f6-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR\_DSOP\_DS\_SELECTION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558f6-106">"CFSTR \_ DSOP \_ DS \_ SELECTION \_ LIST"</span><span class="sxs-lookup"><span data-stu-id="558f6-106">"CFSTR\_DSOP\_DS\_SELECTION\_LIST"</span></span>
</dt> <dt>



<span data-ttu-id="558f6-107">**CFSTR \_ DSOP \_ DS \_ 挑選清單剪貼 \_ 簿** 格式是由呼叫 [**IDsObjectPicker：： InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)所取得的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)所提供。</span><span class="sxs-lookup"><span data-stu-id="558f6-107">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format is provided by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtained by calling [**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span></span> <span data-ttu-id="558f6-108">**CFSTR \_ DSOP \_ ds \_ 挑選清單剪貼 \_ 簿** 格式會提供包含 [**DS \_ 選擇 \_ 清單**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)結構的 **HGLOBAL** 。</span><span class="sxs-lookup"><span data-stu-id="558f6-108">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format provides an **HGLOBAL** that contains a [**DS\_SELECTION\_LIST**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) structure.</span></span> <span data-ttu-id="558f6-109">**DS \_ 選擇 \_ 清單** 結構包含在 [目錄物件選擇器](directory-object-picker.md)對話方塊中選取之專案的相關資料。</span><span class="sxs-lookup"><span data-stu-id="558f6-109">The **DS\_SELECTION\_LIST** structure contains data about the items selected in a [Directory Object Picker](directory-object-picker.md) dialog box.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="558f6-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="558f6-110">Requirements</span></span>



| <span data-ttu-id="558f6-111">需求</span><span class="sxs-lookup"><span data-stu-id="558f6-111">Requirement</span></span> | <span data-ttu-id="558f6-112">值</span><span class="sxs-lookup"><span data-stu-id="558f6-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="558f6-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="558f6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="558f6-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="558f6-114">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="558f6-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="558f6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="558f6-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="558f6-116">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="558f6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="558f6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="558f6-118"><dt>Objsel。h</dt></span><span class="sxs-lookup"><span data-stu-id="558f6-118"><dt>Objsel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="558f6-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="558f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="558f6-120">**DS \_ 選擇 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="558f6-120">**DS\_SELECTION\_LIST**</span></span>](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[<span data-ttu-id="558f6-121">**IDsObjectPicker::InvokeDialog**</span><span class="sxs-lookup"><span data-stu-id="558f6-121">**IDsObjectPicker::InvokeDialog**</span></span>](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[<span data-ttu-id="558f6-122">目錄物件選擇器</span><span class="sxs-lookup"><span data-stu-id="558f6-122">Directory Object Picker</span></span>](directory-object-picker.md)
</dt> </dl>

 

