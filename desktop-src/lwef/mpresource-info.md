---
title: 'MPRESOURCE_INFO 結構 (MpClient .h) '
description: 資源資訊結構。
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO 結構舊版 Windows 環境功能
- PMPRESOURCE_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934644"
---
# <a name="mpresource_info-structure"></a><span data-ttu-id="3c632-105">MPRESOURCE \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="3c632-105">MPRESOURCE\_INFO structure</span></span>

<span data-ttu-id="3c632-106">資源資訊結構。</span><span class="sxs-lookup"><span data-stu-id="3c632-106">Resource information structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c632-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c632-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a><span data-ttu-id="3c632-108">成員</span><span class="sxs-lookup"><span data-stu-id="3c632-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c632-109">**方案**</span><span class="sxs-lookup"><span data-stu-id="3c632-109">**Scheme**</span></span>
</dt> <dd>

<span data-ttu-id="3c632-110">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3c632-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3c632-111">資源配置識別碼，例如 "file" 或 "dir"。</span><span class="sxs-lookup"><span data-stu-id="3c632-111">Resource scheme identifier such as "file" or "dir".</span></span>

</dd> <dt>

<span data-ttu-id="3c632-112">**路徑**</span><span class="sxs-lookup"><span data-stu-id="3c632-112">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="3c632-113">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3c632-113">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3c632-114">資源的絕對路徑（根據 **配置**）。</span><span class="sxs-lookup"><span data-stu-id="3c632-114">Absolute path of resource, based on **Scheme**.</span></span>

</dd> <dt>

<span data-ttu-id="3c632-115">**類別**</span><span class="sxs-lookup"><span data-stu-id="3c632-115">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="3c632-116">Type： **MPRESOURCE \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="3c632-116">Type: **MPRESOURCE\_CLASS**</span></span>

</dd> <dd>

<span data-ttu-id="3c632-117">當資源被識別為威脅的一部分時，就會設定此欄位。</span><span class="sxs-lookup"><span data-stu-id="3c632-117">This field is set when the resource is identified as part of the threat.</span></span> <span data-ttu-id="3c632-118">它會指定資源類別，主要是實體與潛在的。</span><span class="sxs-lookup"><span data-stu-id="3c632-118">It specifies the resource class, mainly concrete vs. latent.</span></span> <span data-ttu-id="3c632-119">它可以是下列可能值的組合：</span><span class="sxs-lookup"><span data-stu-id="3c632-119">It can be a combination of these possible values:</span></span>



| <span data-ttu-id="3c632-120">值</span><span class="sxs-lookup"><span data-stu-id="3c632-120">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="3c632-121">意義</span><span class="sxs-lookup"><span data-stu-id="3c632-121">Meaning</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <span data-ttu-id="3c632-122"><dt>**MP \_資源 \_ 類別 \_ 不明**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="3c632-122"><dt>**MP\_RESOURCE\_CLASS\_UNKNOWN**</dt> <dt>0x0000</dt></span></span> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <span data-ttu-id="3c632-123"><dt>**MP \_資源 \_ 類別 \_ 具體**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="3c632-123"><dt>**MP\_RESOURCE\_CLASS\_CONCRETE**</dt> <dt>0x0001</dt></span></span> </dl>           | <span data-ttu-id="3c632-124">互斥于 **MP \_ 資源類別 \_ 的 \_ 潛在**。</span><span class="sxs-lookup"><span data-stu-id="3c632-124">Mutually exclusive with **MP\_RESOURCE\_CLASS\_LATENT**.</span></span><br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <span data-ttu-id="3c632-125"><dt>**MP \_資源 \_ 類別的 \_ 潛在**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="3c632-125"><dt>**MP\_RESOURCE\_CLASS\_LATENT**</dt> <dt>0x0002</dt></span></span> </dl>                 | <span data-ttu-id="3c632-126">互斥于 **MP \_ 資源類別 \_ 的 \_ 實體**。</span><span class="sxs-lookup"><span data-stu-id="3c632-126">Mutually exclusive with **MP\_RESOURCE\_CLASS\_CONCRETE**.</span></span><br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <span data-ttu-id="3c632-127"><dt>**MP \_資源 \_ 類別 \_ 範例 \_**</dt>檔案 <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="3c632-127"><dt>**MP\_RESOURCE\_CLASS\_SAMPLE\_FILE**</dt> <dt>0x0004</dt></span></span> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <span data-ttu-id="3c632-128"><dt>**MP \_資源 \_ 類別 \_ 共用**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="3c632-128"><dt>**MP\_RESOURCE\_CLASS\_SHARED**</dt> <dt>0x0100</dt></span></span> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c632-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c632-129">Requirements</span></span>



| <span data-ttu-id="3c632-130">需求</span><span class="sxs-lookup"><span data-stu-id="3c632-130">Requirement</span></span> | <span data-ttu-id="3c632-131">值</span><span class="sxs-lookup"><span data-stu-id="3c632-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c632-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c632-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3c632-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c632-133">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3c632-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c632-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3c632-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c632-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c632-136">標頭</span><span class="sxs-lookup"><span data-stu-id="3c632-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c632-137"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c632-137"><dt>MpClient.h</dt></span></span> </dl> |



 

 





