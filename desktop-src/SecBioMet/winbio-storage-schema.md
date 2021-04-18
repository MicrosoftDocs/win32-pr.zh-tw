---
title: 'WINBIO_STORAGE_SCHEMA 結構 (Winbio \_ 類型 .h) '
description: 描述生物特徵辨識存儲裝置配接器的功能。
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- WINBIO_STORAGE_SCHEMA 結構 Windows 生物特徵辨識架構 API
- PWINBIO_STORAGE_SCHEMA 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965948"
---
# <a name="winbio_storage_schema-structure"></a><span data-ttu-id="c49f6-105">WINBIO \_ 儲存體 \_ 架構結構</span><span class="sxs-lookup"><span data-stu-id="c49f6-105">WINBIO\_STORAGE\_SCHEMA structure</span></span>

<span data-ttu-id="c49f6-106">**WINBIO \_ 儲存體 \_ 架構** 結構描述生物特徵辨識儲存體介面卡的功能。</span><span class="sxs-lookup"><span data-stu-id="c49f6-106">The **WINBIO\_STORAGE\_SCHEMA** structure describes the capabilities of a biometric storage adapter.</span></span> <span data-ttu-id="c49f6-107">[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)函數會使用這個結構。</span><span class="sxs-lookup"><span data-stu-id="c49f6-107">This structure is used by the [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c49f6-108">語法</span><span class="sxs-lookup"><span data-stu-id="c49f6-108">Syntax</span></span>


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="c49f6-109">成員</span><span class="sxs-lookup"><span data-stu-id="c49f6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c49f6-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="c49f6-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="c49f6-111">儲存在資料庫中的生物特徵辨識測量型別。</span><span class="sxs-lookup"><span data-stu-id="c49f6-111">The type of biometric measurement saved in the database.</span></span>

</dd> <dt>

<span data-ttu-id="c49f6-112">**DatabaseId**</span><span class="sxs-lookup"><span data-stu-id="c49f6-112">**DatabaseId**</span></span>
</dt> <dd>

<span data-ttu-id="c49f6-113">識別資料庫的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c49f6-113">A GUID that identifies the database.</span></span>

</dd> <dt>

<span data-ttu-id="c49f6-114">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="c49f6-114">**DataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="c49f6-115">識別資料庫中範本格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c49f6-115">A GUID that identifies the format of the templates in the database.</span></span>

</dd> <dt>

<span data-ttu-id="c49f6-116">**屬性**</span><span class="sxs-lookup"><span data-stu-id="c49f6-116">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="c49f6-117">資料庫特性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c49f6-117">Information about the characteristics of the database.</span></span> <span data-ttu-id="c49f6-118">這可以是下列常數的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="c49f6-118">This can be a bitwise **OR** of the following constants.</span></span>



| <span data-ttu-id="c49f6-119">值</span><span class="sxs-lookup"><span data-stu-id="c49f6-119">Value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="c49f6-120">意義</span><span class="sxs-lookup"><span data-stu-id="c49f6-120">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="c49f6-121"><dt>**WINBIO \_資料庫 \_ 旗標 \_ 遮罩**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-121"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="c49f6-122">代表旗標位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="c49f6-122">Represents a mask for the flag bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="c49f6-123"><dt>**WINBIO \_資料庫 \_ 旗標 \_ 遠端**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-123"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="c49f6-124">資料庫位於遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="c49f6-124">The database resides on a remote computer.</span></span><br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="c49f6-125"><dt>**WINBIO \_資料庫 \_ 旗標 \_ 可移動**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-125"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="c49f6-126">資料庫位於抽取式磁碟機上。</span><span class="sxs-lookup"><span data-stu-id="c49f6-126">The database resides on a removable drive.</span></span><br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="c49f6-127"><dt>**WINBIO \_資料庫 \_ 類型 \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-127"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="c49f6-128">資料庫是由資料庫管理系統所管理。</span><span class="sxs-lookup"><span data-stu-id="c49f6-128">The database is managed by a database management system.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="c49f6-129"><dt>**WINBIO \_資料庫 \_ 類型 \_**</dt>檔 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-129"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="c49f6-130">資料庫包含在檔案中。</span><span class="sxs-lookup"><span data-stu-id="c49f6-130">The database is contained in a file.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="c49f6-131"><dt>**WINBIO \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-131"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="c49f6-132">表示類型位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="c49f6-132">Represents a mask for the type bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="c49f6-133"><dt>**WINBIO \_資料庫 \_ 類型 \_ ONCHIP**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-133"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="c49f6-134">資料庫位於生物特徵辨識感應器上。</span><span class="sxs-lookup"><span data-stu-id="c49f6-134">The database resides on the biometric sensor.</span></span><br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="c49f6-135"><dt>**WINBIO \_資料庫 \_ 類型 \_ 智慧卡**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-135"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="c49f6-136">資料庫位於智慧卡上。</span><span class="sxs-lookup"><span data-stu-id="c49f6-136">The database resides on a smart card.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="c49f6-137">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="c49f6-137">**FilePath**</span></span>
</dt> <dd>

<span data-ttu-id="c49f6-138">如果資料庫位於電腦磁片上，則為資料庫的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="c49f6-138">The path and file name of the database if it resides on the computer disk.</span></span>

</dd> <dt>

<span data-ttu-id="c49f6-139">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="c49f6-139">**ConnectionString**</span></span>
</dt> <dd>

<span data-ttu-id="c49f6-140">可傳送至資料庫伺服器以識別資料庫的字串值。</span><span class="sxs-lookup"><span data-stu-id="c49f6-140">A string value that can be sent to a database server to identify the database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c49f6-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="c49f6-141">Requirements</span></span>



| <span data-ttu-id="c49f6-142">需求</span><span class="sxs-lookup"><span data-stu-id="c49f6-142">Requirement</span></span> | <span data-ttu-id="c49f6-143">值</span><span class="sxs-lookup"><span data-stu-id="c49f6-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c49f6-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c49f6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c49f6-145">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c49f6-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c49f6-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c49f6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c49f6-147">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c49f6-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c49f6-148">標頭</span><span class="sxs-lookup"><span data-stu-id="c49f6-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="c49f6-149"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-149"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c49f6-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c49f6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49f6-151">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="c49f6-151">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="c49f6-152">**WinBioEnumDatabases**</span><span class="sxs-lookup"><span data-stu-id="c49f6-152">**WinBioEnumDatabases**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





