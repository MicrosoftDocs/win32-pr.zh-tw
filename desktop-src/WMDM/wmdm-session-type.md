---
title: WMDM_SESSION_TYPE 列舉
description: WMDM \_ 會話 \_ 類型列舉型別會定義會話類型。
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977623"
---
# <a name="wmdm_session_type-enumeration"></a><span data-ttu-id="fac48-104">WMDM \_ 會話 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="fac48-104">WMDM\_SESSION\_TYPE enumeration</span></span>

<span data-ttu-id="fac48-105">**WMDM \_ 會話 \_ 類型** 列舉型別會定義會話類型。</span><span class="sxs-lookup"><span data-stu-id="fac48-105">The **WMDM\_SESSION\_TYPE** enumeration type defines the session type.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac48-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fac48-106">Syntax</span></span>


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="fac48-107">常數</span><span class="sxs-lookup"><span data-stu-id="fac48-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fac48-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ 會話 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="fac48-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM\_SESSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="fac48-109">未定義會話。</span><span class="sxs-lookup"><span data-stu-id="fac48-109">The session is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="fac48-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM \_ 會話 \_ 傳送 \_ 至 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="fac48-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM\_SESSION\_TRANSFER\_TO\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="fac48-111">此會話定義為將資料傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="fac48-111">The session is defined as transferring data to the device.</span></span>

</dd> <dt>

<span data-ttu-id="fac48-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ \_ 從裝置 WMDM 會話 \_ 傳送**</span><span class="sxs-lookup"><span data-stu-id="fac48-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM\_SESSION\_TRANSFER\_FROM\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="fac48-113">此會話定義為從裝置傳送資料。</span><span class="sxs-lookup"><span data-stu-id="fac48-113">The session is defined as transferring data from the device.</span></span>

</dd> <dt>

<span data-ttu-id="fac48-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM \_ 會話 \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="fac48-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM\_SESSION\_DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="fac48-115">此會話定義為刪除資料。</span><span class="sxs-lookup"><span data-stu-id="fac48-115">The session is defined as deleting data.</span></span>

</dd> <dt>

<span data-ttu-id="fac48-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM \_ 會話 \_ 自訂**</span><span class="sxs-lookup"><span data-stu-id="fac48-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM\_SESSION\_CUSTOM**</span></span>
</dt> <dd>

<span data-ttu-id="fac48-117">此會話定義為自訂會話。</span><span class="sxs-lookup"><span data-stu-id="fac48-117">The session is defined as a custom session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fac48-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fac48-118">Requirements</span></span>



| <span data-ttu-id="fac48-119">需求</span><span class="sxs-lookup"><span data-stu-id="fac48-119">Requirement</span></span> | <span data-ttu-id="fac48-120">值</span><span class="sxs-lookup"><span data-stu-id="fac48-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fac48-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fac48-121">Header</span></span><br/> | <dl> <span data-ttu-id="fac48-122"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fac48-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac48-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fac48-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac48-124">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="fac48-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





