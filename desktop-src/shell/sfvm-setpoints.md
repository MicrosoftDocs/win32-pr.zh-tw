---
description: 將目前所選物件的點設定為複製和剪下命令上的資料物件。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_SETPOINTS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195327"
---
# <a name="sfvm_setpoints-message"></a><span data-ttu-id="6c421-104">SFVM \_ SETPOINTS 訊息</span><span class="sxs-lookup"><span data-stu-id="6c421-104">SFVM\_SETPOINTS message</span></span>

<span data-ttu-id="6c421-105">將目前所選物件的點設定為 **複製** 和 **剪** 下命令上的資料物件。</span><span class="sxs-lookup"><span data-stu-id="6c421-105">Sets the points of the currently selected objects to the data object on **Copy** and **Cut** commands.</span></span> <span data-ttu-id="6c421-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="6c421-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a><span data-ttu-id="6c421-107">參數</span><span class="sxs-lookup"><span data-stu-id="6c421-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c421-108">*pdtobj* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c421-108">*pdtobj* \[in\]</span></span>
</dt> <dd><span data-ttu-id="6c421-109">**複製** 和 **剪** 下命令之 <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a>的指標。</span><span class="sxs-lookup"><span data-stu-id="6c421-109">A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> of the **Copy** and **Cut** commands.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c421-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c421-110">Return value</span></span>

<span data-ttu-id="6c421-111">永遠傳回零。</span><span class="sxs-lookup"><span data-stu-id="6c421-111">Always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c421-112">備註</span><span class="sxs-lookup"><span data-stu-id="6c421-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6c421-113">需求</span><span class="sxs-lookup"><span data-stu-id="6c421-113">Requirements</span></span>



| <span data-ttu-id="6c421-114">需求</span><span class="sxs-lookup"><span data-stu-id="6c421-114">Requirement</span></span> | <span data-ttu-id="6c421-115">值</span><span class="sxs-lookup"><span data-stu-id="6c421-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c421-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c421-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c421-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c421-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6c421-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c421-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c421-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c421-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c421-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6c421-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c421-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c421-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
