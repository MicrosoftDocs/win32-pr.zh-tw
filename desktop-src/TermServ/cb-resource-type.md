---
title: 'CB_RESOURCE_TYPE 列舉 (Cbclient .h) '
description: 指定連入連接所連線的資源類型。
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685678"
---
# <a name="cb_resource_type-enumeration"></a><span data-ttu-id="daef8-104">CB \_ 資源 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="daef8-104">CB\_RESOURCE\_TYPE enumeration</span></span>

<span data-ttu-id="daef8-105">指定連入連接所連線的資源類型。</span><span class="sxs-lookup"><span data-stu-id="daef8-105">Specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="daef8-106">此列舉會搭配 [**CB \_ 連接 \_ 資訊**](cb-connection-info.md) 結構使用。</span><span class="sxs-lookup"><span data-stu-id="daef8-106">This enumeration is used with the [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="daef8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="daef8-107">Syntax</span></span>


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="daef8-108">常數</span><span class="sxs-lookup"><span data-stu-id="daef8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="daef8-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB \_ 資源 \_ 未定義**</span><span class="sxs-lookup"><span data-stu-id="daef8-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB\_RESOURCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="daef8-110">資源類型未定義。</span><span class="sxs-lookup"><span data-stu-id="daef8-110">The resource type is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="daef8-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB \_ 資源 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="daef8-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB\_RESOURCE\_SESSION**</span></span>
</dt> <dd>

<span data-ttu-id="daef8-112">資源是遠端會話。</span><span class="sxs-lookup"><span data-stu-id="daef8-112">The resource is a remote session.</span></span>

</dd> <dt>

<span data-ttu-id="daef8-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB \_ 資源 \_ VM**</span><span class="sxs-lookup"><span data-stu-id="daef8-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB\_RESOURCE\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="daef8-114">資源是一種虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="daef8-114">The resource is a virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="daef8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="daef8-115">Requirements</span></span>



| <span data-ttu-id="daef8-116">需求</span><span class="sxs-lookup"><span data-stu-id="daef8-116">Requirement</span></span> | <span data-ttu-id="daef8-117">值</span><span class="sxs-lookup"><span data-stu-id="daef8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="daef8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="daef8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="daef8-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="daef8-119">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="daef8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="daef8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="daef8-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="daef8-121">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="daef8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="daef8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="daef8-123"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="daef8-123"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daef8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="daef8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daef8-125">**CB \_ 連接 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="daef8-125">**CB\_CONNECTION\_INFO**</span></span>](cb-connection-info.md)
</dt> </dl>

 

 





