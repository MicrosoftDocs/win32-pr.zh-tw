---
title: IMAPI.EXE 常數
description: IMAPI.EXE 會定義下列常數。
ms.assetid: 3ae67227-1cee-4e9c-a7fe-228de596030a
topic_type:
- apiref
api_name:
- IMAPI_SECTOR_SIZE
- IMAPI_SECTORS_PER_SECOND_AT_1X_CD
- IMAPI_SECTORS_PER_SECOND_AT_1X_DVD
- IMAPI_SECTORS_PER_SECOND_AT_1X_BD
api_location:
- Imapi2.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb8c6ac1d855509e67ce5e066410f107172d2ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979677"
---
# <a name="imapi-constants"></a><span data-ttu-id="95663-103">IMAPI.EXE 常數</span><span class="sxs-lookup"><span data-stu-id="95663-103">IMAPI Constants</span></span>

<span data-ttu-id="95663-104">IMAPI.EXE 會定義下列常數。</span><span class="sxs-lookup"><span data-stu-id="95663-104">IMAPI defines the following constants.</span></span>



| <span data-ttu-id="95663-105">常數</span><span class="sxs-lookup"><span data-stu-id="95663-105">Constant</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="95663-106">描述</span><span class="sxs-lookup"><span data-stu-id="95663-106">Description</span></span>                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="IMAPI_SECTOR_SIZE"></span><span id="imapi_sector_size"></span><dl> <span data-ttu-id="95663-107"><dt>**IMAPI.EXE \_ 磁區 \_ 大小**</dt></span><span class="sxs-lookup"><span data-stu-id="95663-107"><dt>**IMAPI\_SECTOR\_SIZE**</dt></span></span> </dl>                                                        | <span data-ttu-id="95663-108">磁區中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="95663-108">Number of bytes in a sector.</span></span><br/>                                                  |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_CD"></span><span id="imapi_sectors_per_second_at_1x_cd"></span><dl> <span data-ttu-id="95663-109"><dt>**\_每秒 imapi.exe 個磁區 \_ \_ ，第1個 \_ \_ \_ 光碟**</dt></span><span class="sxs-lookup"><span data-stu-id="95663-109"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_CD**</dt></span></span> </dl>    | <span data-ttu-id="95663-110">CD 旋轉速度的基本速率，以每秒磁區的速率來測量。</span><span class="sxs-lookup"><span data-stu-id="95663-110">Base rate of speed that a CD spins, measured in sectors per second.</span></span><br/>           |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_DVD"></span><span id="imapi_sectors_per_second_at_1x_dvd"></span><dl> <span data-ttu-id="95663-111"><dt>**\_每秒 imapi.exe 個磁區 \_ \_ ，第 1 \_ 部 \_ \_ DVD**</dt></span><span class="sxs-lookup"><span data-stu-id="95663-111"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_DVD**</dt></span></span> </dl> | <span data-ttu-id="95663-112">DVD 旋轉的基本速率，以每秒的磁區來測量。</span><span class="sxs-lookup"><span data-stu-id="95663-112">Base rate of speed that a DVD spins, measured in sectors per second.</span></span><br/>          |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_BD"></span><span id="imapi_sectors_per_second_at_1x_bd"></span><dl> <span data-ttu-id="95663-113"><dt>**\_每秒 Imapi.exe 磁區（ \_ 每 \_ 秒） \_ \_ \_ BD**</dt></span><span class="sxs-lookup"><span data-stu-id="95663-113"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_BD**</dt></span></span> </dl>    | <span data-ttu-id="95663-114">藍光光碟旋轉的速率基本速率，以每秒磁區的速率表示。</span><span class="sxs-lookup"><span data-stu-id="95663-114">Base rate of speed that a Blu-ray disc spins, measured in sectors per second.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="95663-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="95663-115">Requirements</span></span>



| <span data-ttu-id="95663-116">需求</span><span class="sxs-lookup"><span data-stu-id="95663-116">Requirement</span></span> | <span data-ttu-id="95663-117">值</span><span class="sxs-lookup"><span data-stu-id="95663-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95663-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95663-118">Minimum supported client</span></span><br/> | <span data-ttu-id="95663-119">Windows Vista、Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95663-119">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="95663-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95663-120">Minimum supported server</span></span><br/> | <span data-ttu-id="95663-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95663-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95663-122">Idl</span><span class="sxs-lookup"><span data-stu-id="95663-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95663-123"><dt>Imapi2 .idl</dt></span><span class="sxs-lookup"><span data-stu-id="95663-123"><dt>Imapi2.idl</dt></span></span> </dl> |



 

 





