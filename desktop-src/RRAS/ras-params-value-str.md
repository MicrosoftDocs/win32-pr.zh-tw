---
title: 'RAS_PARAMS_VALUE 聯集 (Rassapi .h) '
description: Ras \_ \_ 參數值 UNION 在 ras 參數結構中用 \_ 來儲存與媒體特定參數相關聯的資料。
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS_PARAMS_VALUE 聯集 RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093780"
---
# <a name="ras_params_value-union"></a><span data-ttu-id="0ddd3-104">RAS \_ PARAMS \_ 值聯集</span><span class="sxs-lookup"><span data-stu-id="0ddd3-104">RAS\_PARAMS\_VALUE union</span></span>

<span data-ttu-id="0ddd3-105">\[Windows Vista 不支援 **RAS \_ PARAMS \_ 值** 聯集。\]</span><span class="sxs-lookup"><span data-stu-id="0ddd3-105">\[The **RAS\_PARAMS\_VALUE** union is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="0ddd3-106">Ras **參數 \_ \_ 值** union 在 [**ras \_ 參數**](ras-parameters-str.md) 結構中用來儲存與媒體特定參數相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-106">The **RAS\_PARAMS\_VALUE** union is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to store the data associated with a media-specific parameter.</span></span> <span data-ttu-id="0ddd3-107">**Ras \_ 參數** 結構的 **P \_ 類型** 成員會使用 [**ras \_ params \_ 格式**](ras-params-format-str.md)列舉的值，來指出目前儲存在 **ras \_ 參數 \_ 值** 中的數值型別。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-107">The **P\_Type** member of the **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the type of value currently stored in **RAS\_PARAMS\_VALUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddd3-108">語法</span><span class="sxs-lookup"><span data-stu-id="0ddd3-108">Syntax</span></span>


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a><span data-ttu-id="0ddd3-109">成員</span><span class="sxs-lookup"><span data-stu-id="0ddd3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ddd3-110">**Number**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-110">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="0ddd3-111">如果 [**RAS \_ 參數**](ras-parameters-str.md)結構的 **P \_ 類型** 成員是 ParamNumber，則 **數位** 成員會包含媒體專用參數的值。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-111">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="0ddd3-112">例如，MAXCONNECTBPS 參數的類型是 ParamNumber，而值可能是19200。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-112">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

<span data-ttu-id="0ddd3-113">如果 [**RAS \_ 參數**](ras-parameters-str.md)結構的 **P \_ 類型** 成員是 ParamNumber，則 **數位** 成員會包含媒體專用參數的值。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-113">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="0ddd3-114">例如，MAXCONNECTBPS 參數的類型是 ParamNumber，而值可能是19200。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-114">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

</dd> <dt>

<span data-ttu-id="0ddd3-115">**String**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-115">**String**</span></span>
</dt> <dd>

<span data-ttu-id="0ddd3-116">如果 [**RAS \_ 參數**](ras-parameters-str.md)結構的 **P \_ 類型** 成員是 ParamString，則 **字串** 成員會包含媒體專用參數的值。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-116">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamString, the **String** member contains the value of the media-specific parameter.</span></span>

<dl> <dt>

<span data-ttu-id="0ddd3-117">**長度**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-117">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="0ddd3-118">指定 **資料** 成員所指向之字串的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-118">Specifies the length, in characters, of the string pointed to by the **Data** member.</span></span>

</dd> <dt>

<span data-ttu-id="0ddd3-119">**資料**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-119">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="0ddd3-120">緩衝區的指標，此緩衝區包含媒體特定參數的字串值。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-120">Pointer to a buffer that contains the string value of a media-specific parameter.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ddd3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ddd3-121">Requirements</span></span>



| <span data-ttu-id="0ddd3-122">需求</span><span class="sxs-lookup"><span data-stu-id="0ddd3-122">Requirement</span></span> | <span data-ttu-id="0ddd3-123">值</span><span class="sxs-lookup"><span data-stu-id="0ddd3-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddd3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ddd3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddd3-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddd3-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0ddd3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ddd3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddd3-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddd3-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0ddd3-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0ddd3-128">End of client support</span></span><br/>    | <span data-ttu-id="0ddd3-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ddd3-129">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="0ddd3-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0ddd3-130">End of server support</span></span><br/>    | <span data-ttu-id="0ddd3-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0ddd3-131">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="0ddd3-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0ddd3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ddd3-133"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddd3-133"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddd3-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ddd3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddd3-135">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="0ddd3-135">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="0ddd3-136">RAS 伺服器管理聯集</span><span class="sxs-lookup"><span data-stu-id="0ddd3-136">RAS Server Administration Union</span></span>](ras-server-administration-union.md)
</dt> <dt>

[<span data-ttu-id="0ddd3-137">**RAS \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-137">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="0ddd3-138">**RAS \_ 參數 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-138">**RAS\_PARAMS\_FORMAT**</span></span>](ras-params-format-str.md)
</dt> </dl>

 

 





