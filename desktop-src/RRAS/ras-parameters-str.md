---
title: 'RAS_PARAMETERS 結構 (Rassapi .h) '
description: RasAdminPortGetInfo 函 \_ 式會使用 ras 參數結構，傳回與 RAS 伺服器上端口相關聯之媒體特定參數的名稱和值。
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509071"
---
# <a name="ras_parameters-structure"></a><span data-ttu-id="aa92e-104">RAS \_ 參數結構</span><span class="sxs-lookup"><span data-stu-id="aa92e-104">RAS\_PARAMETERS structure</span></span>

<span data-ttu-id="aa92e-105">\[Windows Vista 不支援 **RAS \_ 參數** 結構。\]</span><span class="sxs-lookup"><span data-stu-id="aa92e-105">\[The **RAS\_PARAMETERS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="aa92e-106">[**RasAdminPortGetInfo**](rasadminportgetinfo.md)函式會使用 **ras \_ 參數** 結構，傳回與 RAS 伺服器上端口相關聯之媒體特定參數的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="aa92e-106">The **RAS\_PARAMETERS** structure is used by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to return the name and value of a media-specific parameter associated with a port on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa92e-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa92e-107">Syntax</span></span>


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="aa92e-108">成員</span><span class="sxs-lookup"><span data-stu-id="aa92e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa92e-109">**P \_ 鍵**</span><span class="sxs-lookup"><span data-stu-id="aa92e-109">**P\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="aa92e-110">指定代表媒體特定參數的索引鍵名稱，例如 MAXCONNECTBPS。</span><span class="sxs-lookup"><span data-stu-id="aa92e-110">Specifies the name of the key that represents the media-specific parameter, such as MAXCONNECTBPS.</span></span>

</dd> <dt>

<span data-ttu-id="aa92e-111">**P \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="aa92e-111">**P\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="aa92e-112">識別與參數相關聯的資料類型。</span><span class="sxs-lookup"><span data-stu-id="aa92e-112">Identifies the type of data associated with the parameter.</span></span> <span data-ttu-id="aa92e-113">這個成員可以是下列其中一個 [**RAS \_ PARAMS \_ 格式**](ras-params-format-str.md) 列舉值的值。</span><span class="sxs-lookup"><span data-stu-id="aa92e-113">This member can be one of the following values from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration.</span></span>



| <span data-ttu-id="aa92e-114">值</span><span class="sxs-lookup"><span data-stu-id="aa92e-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="aa92e-115">意義</span><span class="sxs-lookup"><span data-stu-id="aa92e-115">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <span data-ttu-id="aa92e-116"><dt>**ParamNumber**</dt></span><span class="sxs-lookup"><span data-stu-id="aa92e-116"><dt>**ParamNumber**</dt></span></span> </dl> | <span data-ttu-id="aa92e-117">指出與索引鍵相關聯的資料是數位。</span><span class="sxs-lookup"><span data-stu-id="aa92e-117">Indicates that the data associated with the key is a number.</span></span><br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <span data-ttu-id="aa92e-118"><dt>**ParamString**</dt></span><span class="sxs-lookup"><span data-stu-id="aa92e-118"><dt>**ParamString**</dt></span></span> </dl> | <span data-ttu-id="aa92e-119">表示與索引鍵相關聯的資料為字串。</span><span class="sxs-lookup"><span data-stu-id="aa92e-119">Indicates that the data associated with the key is a string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aa92e-120">**P \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="aa92e-120">**P\_Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="aa92e-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="aa92e-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aa92e-122">**P \_ 值**</span><span class="sxs-lookup"><span data-stu-id="aa92e-122">**P\_Value**</span></span>
</dt> <dd>

<span data-ttu-id="aa92e-123">指定與參數相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="aa92e-123">Specifies the value associated with the parameter.</span></span> <span data-ttu-id="aa92e-124">這個成員是 [**RAS \_ PARAMS \_ 值**](ras-params-value-str.md) 聯集。</span><span class="sxs-lookup"><span data-stu-id="aa92e-124">This member is a [**RAS\_PARAMS\_VALUE**](ras-params-value-str.md) union.</span></span> <span data-ttu-id="aa92e-125">如果 **P \_ 類型** 成員是 ParamNumber，等位的 **數位** 成員就會包含此值。</span><span class="sxs-lookup"><span data-stu-id="aa92e-125">If the **P\_Type** member is ParamNumber, the **Number** member of the union contains the value.</span></span> <span data-ttu-id="aa92e-126">如果 **P \_ 類型** 是 ParamString，等位的 **字串** 成員就會包含值。</span><span class="sxs-lookup"><span data-stu-id="aa92e-126">If **P\_Type** is ParamString, the **String** member of the union contains the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa92e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa92e-127">Requirements</span></span>



| <span data-ttu-id="aa92e-128">需求</span><span class="sxs-lookup"><span data-stu-id="aa92e-128">Requirement</span></span> | <span data-ttu-id="aa92e-129">值</span><span class="sxs-lookup"><span data-stu-id="aa92e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa92e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa92e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa92e-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa92e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aa92e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa92e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa92e-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa92e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aa92e-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="aa92e-134">End of client support</span></span><br/>    | <span data-ttu-id="aa92e-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa92e-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="aa92e-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="aa92e-136">End of server support</span></span><br/>    | <span data-ttu-id="aa92e-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa92e-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="aa92e-138">標頭</span><span class="sxs-lookup"><span data-stu-id="aa92e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa92e-139"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa92e-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa92e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa92e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa92e-141">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="aa92e-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="aa92e-142">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="aa92e-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="aa92e-143">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="aa92e-143">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="aa92e-144">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="aa92e-144">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="aa92e-145">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="aa92e-145">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





