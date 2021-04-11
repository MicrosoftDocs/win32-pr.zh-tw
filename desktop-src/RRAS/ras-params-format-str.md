---
title: 'RAS_PARAMS_FORMAT 列舉 (Rassapi .h) '
description: Ras \_ \_ 參數格式列舉型別會在 ras \_ 參數結構中用來指出與媒體特定索引鍵相關聯的資料類型。
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT 列舉 RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104393"
---
# <a name="ras_params_format-enumeration"></a><span data-ttu-id="5a3d3-104">RAS \_ 參數 \_ 格式列舉</span><span class="sxs-lookup"><span data-stu-id="5a3d3-104">RAS\_PARAMS\_FORMAT enumeration</span></span>

<span data-ttu-id="5a3d3-105">\[Windows Vista 不支援 **RAS \_ PARAMS \_ 格式** 列舉。\]</span><span class="sxs-lookup"><span data-stu-id="5a3d3-105">\[The **RAS\_PARAMS\_FORMAT** enumeration is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="5a3d3-106">Ras **參數 \_ \_ 格式** 列舉型別會在 [**ras \_ 參數**](ras-parameters-str.md) 結構中用來指出與媒體特定索引鍵相關聯的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5a3d3-106">The **RAS\_PARAMS\_FORMAT** enumeration type is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to indicate the type of data associated with a media-specific key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a3d3-107">Syntax</span></span>


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="5a3d3-108">常數</span><span class="sxs-lookup"><span data-stu-id="5a3d3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5a3d3-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span><span class="sxs-lookup"><span data-stu-id="5a3d3-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5a3d3-110">指出與索引鍵相關聯的資料是數位。</span><span class="sxs-lookup"><span data-stu-id="5a3d3-110">Indicates that the data associated with the key is a number.</span></span>

</dd> <dt>

<span data-ttu-id="5a3d3-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span><span class="sxs-lookup"><span data-stu-id="5a3d3-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span></span>
</dt> <dd>

<span data-ttu-id="5a3d3-112">表示與索引鍵相關聯的資料為字串。</span><span class="sxs-lookup"><span data-stu-id="5a3d3-112">Indicates that the data associated with the key is a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a3d3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a3d3-113">Requirements</span></span>



| <span data-ttu-id="5a3d3-114">需求</span><span class="sxs-lookup"><span data-stu-id="5a3d3-114">Requirement</span></span> | <span data-ttu-id="5a3d3-115">值</span><span class="sxs-lookup"><span data-stu-id="5a3d3-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3d3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a3d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3d3-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a3d3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5a3d3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a3d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3d3-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a3d3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5a3d3-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5a3d3-120">End of client support</span></span><br/>    | <span data-ttu-id="5a3d3-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a3d3-121">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="5a3d3-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5a3d3-122">End of server support</span></span><br/>    | <span data-ttu-id="5a3d3-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a3d3-123">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="5a3d3-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5a3d3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3d3-125"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3d3-125"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3d3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a3d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3d3-127">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="5a3d3-127">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="5a3d3-128">RAS 伺服器管理列舉</span><span class="sxs-lookup"><span data-stu-id="5a3d3-128">RAS Server Administration Enumerations</span></span>](ras-server-administration-enumerations.md)
</dt> <dt>

[<span data-ttu-id="5a3d3-129">**RAS \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="5a3d3-129">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> </dl>

 

 





