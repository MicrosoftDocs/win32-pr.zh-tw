---
description: 取得視圖的屬性。
title: IShellFolderViewType：： GetViewTypeProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842699"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="9fefb-103">IShellFolderViewType：： GetViewTypeProperties 方法</span><span class="sxs-lookup"><span data-stu-id="9fefb-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="9fefb-104">取得視圖的屬性。</span><span class="sxs-lookup"><span data-stu-id="9fefb-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fefb-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fefb-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9fefb-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fefb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fefb-107">*pidl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fefb-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fefb-108">類型： **PCUITEMID \_ 子** 系</span><span class="sxs-lookup"><span data-stu-id="9fefb-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="9fefb-109">PIDL。</span><span class="sxs-lookup"><span data-stu-id="9fefb-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="9fefb-110">*pdwFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9fefb-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fefb-111">類型： **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="9fefb-111">Type: **DWORD\***</span></span>

<span data-ttu-id="9fefb-112">不帶正負號整數變數的指標，此變數會接收 view 屬性，表示選取視圖時該怎麼辦。</span><span class="sxs-lookup"><span data-stu-id="9fefb-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="9fefb-113">旗標可以是下列值的任何組合。</span><span class="sxs-lookup"><span data-stu-id="9fefb-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="9fefb-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_通知 \_ CREATE** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="9fefb-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG\_NOTIFY\_CREATE** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="9fefb-115">建立視圖專案（如果沒有的話）。</span><span class="sxs-lookup"><span data-stu-id="9fefb-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="9fefb-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_通知 \_ 手段** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="9fefb-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="9fefb-117">重新插入 PIDL 並重新排序。</span><span class="sxs-lookup"><span data-stu-id="9fefb-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fefb-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fefb-118">Return value</span></span>

<span data-ttu-id="9fefb-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9fefb-119">Type: **HRESULT**</span></span>

<span data-ttu-id="9fefb-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9fefb-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9fefb-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9fefb-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fefb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fefb-122">Requirements</span></span>



| <span data-ttu-id="9fefb-123">需求</span><span class="sxs-lookup"><span data-stu-id="9fefb-123">Requirement</span></span> | <span data-ttu-id="9fefb-124">值</span><span class="sxs-lookup"><span data-stu-id="9fefb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fefb-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9fefb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9fefb-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fefb-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9fefb-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9fefb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9fefb-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fefb-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9fefb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9fefb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fefb-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fefb-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




