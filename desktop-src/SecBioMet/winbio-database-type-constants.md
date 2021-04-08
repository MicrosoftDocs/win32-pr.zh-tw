---
title: 'WINBIO_DATABASE_TYPE 常數 (Winbio \_ 類型 .h) '
description: 可以用於 WINBIO \_ 儲存架構結構之屬性成員的旗標 \_ 。
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685914"
---
# <a name="winbio_database_type-constants"></a><span data-ttu-id="2a363-103">WINBIO \_ 資料庫 \_ 類型常數</span><span class="sxs-lookup"><span data-stu-id="2a363-103">WINBIO\_DATABASE\_TYPE Constants</span></span>

<span data-ttu-id="2a363-104">下列旗標可用於 [**WINBIO \_ 儲存 \_ 架構**](winbio-storage-schema.md)結構的 **屬性** 成員。</span><span class="sxs-lookup"><span data-stu-id="2a363-104">The following flags can be used for the **Attributes** member of the [**WINBIO\_STORAGE\_SCHEMA**](winbio-storage-schema.md) structure.</span></span>



| <span data-ttu-id="2a363-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="2a363-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="2a363-106">Description</span><span class="sxs-lookup"><span data-stu-id="2a363-106">Description</span></span>                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="2a363-107"><dt>**WINBIO \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-107"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="2a363-108">表示所有 \_ 類型位的遮罩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2a363-108">Represents a mask for all of the \_TYPE\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="2a363-109"><dt>**WINBIO \_資料庫 \_ 類型 \_**</dt>檔 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-109"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="2a363-110">資料庫包含在檔案中。</span><span class="sxs-lookup"><span data-stu-id="2a363-110">The database is contained in a file.</span></span><br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="2a363-111"><dt>**WINBIO \_資料庫 \_ 類型 \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-111"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="2a363-112">資料庫是由外部資料庫管理系統所管理 (DBMS) 元件，例如 Microsoft SQL Server。</span><span class="sxs-lookup"><span data-stu-id="2a363-112">The database is managed by an external database management system (DBMS) component, such as Microsoft SQL Server.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="2a363-113"><dt>**WINBIO \_資料庫 \_ 類型 \_ ONCHIP**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-113"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="2a363-114">資料庫位於生物特徵辨識感應器上。</span><span class="sxs-lookup"><span data-stu-id="2a363-114">The database resides on the biometric sensor.</span></span><br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="2a363-115"><dt>**WINBIO \_資料庫 \_ 類型 \_ 智慧卡**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-115"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="2a363-116">資料庫位於智慧卡上。</span><span class="sxs-lookup"><span data-stu-id="2a363-116">The database resides on a smart card.</span></span><br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="2a363-117"><dt>**WINBIO \_資料庫 \_ 旗標 \_ 遮罩**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-117"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="2a363-118">表示所有旗標位的遮罩 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="2a363-118">Represents a mask for all of the \_FLAG\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="2a363-119"><dt>**WINBIO \_資料庫 \_ 旗標 \_ 可移動**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-119"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="2a363-120">包含資料庫的儲存媒體可以從電腦中實際移除。</span><span class="sxs-lookup"><span data-stu-id="2a363-120">The storage medium containing the database can be physically removed from the computer.</span></span><br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="2a363-121"><dt>**WINBIO \_資料庫 \_ 旗標 \_ 遠端**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="2a363-121"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="2a363-122">資料庫位於遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="2a363-122">The database resides on a remote computer.</span></span><br/>                                                                        |



## <a name="requirements"></a><span data-ttu-id="2a363-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a363-123">Requirements</span></span>



| <span data-ttu-id="2a363-124">需求</span><span class="sxs-lookup"><span data-stu-id="2a363-124">Requirement</span></span> | <span data-ttu-id="2a363-125">值</span><span class="sxs-lookup"><span data-stu-id="2a363-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a363-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a363-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2a363-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a363-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="2a363-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a363-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2a363-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a363-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2a363-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2a363-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a363-131"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2a363-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a363-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a363-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a363-133">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="2a363-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





