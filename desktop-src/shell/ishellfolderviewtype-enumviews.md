---
description: 抓取列舉值，這個列舉值會為每個擴充視圖 (PIDL) 的專案識別碼清單傳回一個指標。
title: IShellFolderViewType：： EnumViews 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842769"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="c37d9-103">IShellFolderViewType：： EnumViews 方法</span><span class="sxs-lookup"><span data-stu-id="c37d9-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="c37d9-104">抓取列舉值，這個列舉值會為每個擴充視圖 (PIDL) 的專案識別碼清單傳回一個指標。</span><span class="sxs-lookup"><span data-stu-id="c37d9-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="c37d9-105">語法</span><span class="sxs-lookup"><span data-stu-id="c37d9-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="c37d9-106">參數</span><span class="sxs-lookup"><span data-stu-id="c37d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c37d9-107">*grfFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c37d9-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c37d9-108">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="c37d9-108">Type: **ULONG**</span></span>

<span data-ttu-id="c37d9-109">旗標，指出列舉中要包含的專案。</span><span class="sxs-lookup"><span data-stu-id="c37d9-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="c37d9-110">如需可能值的清單，請參閱 [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="c37d9-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="c37d9-111">您可以忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="c37d9-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c37d9-112">*ppenum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c37d9-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c37d9-113">類型： **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="c37d9-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="c37d9-114">接收列舉值之 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 型別指標變數的位址。</span><span class="sxs-lookup"><span data-stu-id="c37d9-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c37d9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c37d9-115">Return value</span></span>

<span data-ttu-id="c37d9-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c37d9-116">Type: **HRESULT**</span></span>

<span data-ttu-id="c37d9-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c37d9-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c37d9-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c37d9-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c37d9-119">備註</span><span class="sxs-lookup"><span data-stu-id="c37d9-119">Remarks</span></span>

<span data-ttu-id="c37d9-120">Views 會以 Pidl) 表示的根目錄 (，以隱藏資料夾的形式呈現給使用者。</span><span class="sxs-lookup"><span data-stu-id="c37d9-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="c37d9-121">在適當的情況下，預設 view (off 根資料夾) 會以 **Null** 或空白 PIDL 來表示。</span><span class="sxs-lookup"><span data-stu-id="c37d9-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c37d9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c37d9-122">Requirements</span></span>



| <span data-ttu-id="c37d9-123">需求</span><span class="sxs-lookup"><span data-stu-id="c37d9-123">Requirement</span></span> | <span data-ttu-id="c37d9-124">值</span><span class="sxs-lookup"><span data-stu-id="c37d9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c37d9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c37d9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c37d9-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c37d9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c37d9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c37d9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c37d9-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c37d9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c37d9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c37d9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c37d9-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c37d9-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




