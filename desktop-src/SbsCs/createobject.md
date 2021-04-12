---
description: ActCtx 物件的 CreateObject 方法會在目前資訊清單的內容中建立物件。
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. CreateObject 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193289"
---
# <a name="actctxcreateobject-method"></a><span data-ttu-id="c58a2-103">ActCtx. CreateObject 方法</span><span class="sxs-lookup"><span data-stu-id="c58a2-103">ActCtx.CreateObject method</span></span>

<span data-ttu-id="c58a2-104">[**ActCtx**](microsoft-windows-actctx-object.md)物件的 **CreateObject** 方法會在目前資訊清單的內容中建立物件。</span><span class="sxs-lookup"><span data-stu-id="c58a2-104">The **CreateObject** method of the [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object creates an object in the context of the current manifest.</span></span>

## <a name="syntax"></a><span data-ttu-id="c58a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c58a2-105">Syntax</span></span>


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a><span data-ttu-id="c58a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c58a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c58a2-107">*objectId*</span><span class="sxs-lookup"><span data-stu-id="c58a2-107">*objectId*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a2-108">字串，指定要建立之物件的類型。</span><span class="sxs-lookup"><span data-stu-id="c58a2-108">A string that specifies the type of object to create.</span></span> <span data-ttu-id="c58a2-109">例如，COM ProgID。</span><span class="sxs-lookup"><span data-stu-id="c58a2-109">For example, a COM ProgID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c58a2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c58a2-110">Return value</span></span>

<span data-ttu-id="c58a2-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c58a2-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c58a2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c58a2-112">Requirements</span></span>



| <span data-ttu-id="c58a2-113">需求</span><span class="sxs-lookup"><span data-stu-id="c58a2-113">Requirement</span></span> | <span data-ttu-id="c58a2-114">值</span><span class="sxs-lookup"><span data-stu-id="c58a2-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c58a2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c58a2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c58a2-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c58a2-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c58a2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c58a2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c58a2-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c58a2-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c58a2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c58a2-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c58a2-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c58a2-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="c58a2-121">IID</span><span class="sxs-lookup"><span data-stu-id="c58a2-121">IID</span></span><br/>                      | <span data-ttu-id="c58a2-122">IID \_ IActCtx 定義為8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="c58a2-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c58a2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c58a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c58a2-124">**GetObject 方法**</span><span class="sxs-lookup"><span data-stu-id="c58a2-124">**GetObject Method**</span></span>](getobject.md)
</dt> </dl>

 

 




