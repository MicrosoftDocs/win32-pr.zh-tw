---
title: 'Delete 方法 (WSManDisp) '
description: 刪除資源 URI 中指定的資源。
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Delete 方法 Windows 遠端管理
- Delete 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理、Delete 方法
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934107"
---
# <a name="sessiondelete-method"></a><span data-ttu-id="9d963-106">Session. Delete 方法</span><span class="sxs-lookup"><span data-stu-id="9d963-106">Session.Delete method</span></span>

<span data-ttu-id="9d963-107">刪除資源 URI 中指定的資源。</span><span class="sxs-lookup"><span data-stu-id="9d963-107">Deletes the resource specified in the resource URI.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d963-108">語法</span><span class="sxs-lookup"><span data-stu-id="9d963-108">Syntax</span></span>


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9d963-109">參數</span><span class="sxs-lookup"><span data-stu-id="9d963-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d963-110">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d963-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d963-111">要刪除之資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="9d963-111">The URI of the resource to be deleted.</span></span> <span data-ttu-id="9d963-112">您也可以使用 [**ResourceLocator**](resourcelocator.md) 物件來指定資源。</span><span class="sxs-lookup"><span data-stu-id="9d963-112">You can also use a [**ResourceLocator**](resourcelocator.md) object to specify the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9d963-113">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9d963-113">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d963-114">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="9d963-114">Reserved for future use.</span></span> <span data-ttu-id="9d963-115">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="9d963-115">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d963-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d963-116">Return value</span></span>

<span data-ttu-id="9d963-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9d963-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d963-118">備註</span><span class="sxs-lookup"><span data-stu-id="9d963-118">Remarks</span></span>

<span data-ttu-id="9d963-119">下列語法用來呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9d963-119">The following syntax is used to call this method.</span></span>


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a><span data-ttu-id="9d963-120">範例</span><span class="sxs-lookup"><span data-stu-id="9d963-120">Examples</span></span>

<span data-ttu-id="9d963-121">下列 VBScript 程式碼範例會刪除針對 HTTP 傳輸設定的接聽程式。</span><span class="sxs-lookup"><span data-stu-id="9d963-121">The following VBScript code example deletes the listeners configured for HTTP transport.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a><span data-ttu-id="9d963-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d963-122">Requirements</span></span>



| <span data-ttu-id="9d963-123">需求</span><span class="sxs-lookup"><span data-stu-id="9d963-123">Requirement</span></span> | <span data-ttu-id="9d963-124">值</span><span class="sxs-lookup"><span data-stu-id="9d963-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d963-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d963-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d963-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d963-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9d963-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d963-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d963-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d963-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9d963-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9d963-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d963-130"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d963-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d963-131">Idl</span><span class="sxs-lookup"><span data-stu-id="9d963-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d963-132"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d963-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9d963-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d963-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d963-134"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9d963-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9d963-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9d963-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d963-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d963-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d963-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d963-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d963-138">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="9d963-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





