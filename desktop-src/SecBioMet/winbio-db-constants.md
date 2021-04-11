---
title: 'WINBIO_DB 常數 (Winbio \_ 類型 .h) '
description: 指定要用於系統集區的資料庫。
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104369"
---
# <a name="winbio_db-constants"></a><span data-ttu-id="f0ff5-103">WINBIO \_ DB 常數</span><span class="sxs-lookup"><span data-stu-id="f0ff5-103">WINBIO\_DB Constants</span></span>

<span data-ttu-id="f0ff5-104">呼叫 [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) 來指定要用於系統集區的資料庫時，可以使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="f0ff5-104">The following constants can be used when calling [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to specify the database to be used for a system pool.</span></span>



| <span data-ttu-id="f0ff5-105">常數</span><span class="sxs-lookup"><span data-stu-id="f0ff5-105">Constant</span></span>                                                                                                                                                                         | <span data-ttu-id="f0ff5-106">描述</span><span class="sxs-lookup"><span data-stu-id="f0ff5-106">Description</span></span>                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <span data-ttu-id="f0ff5-107"><dt>**WINBIO \_ DB \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ff5-107"><dt>**WINBIO\_DB\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="f0ff5-108">感應器集區中的每個生物特徵辨識單位都會使用預設生物識別單位設定中指定的預設資料庫。</span><span class="sxs-lookup"><span data-stu-id="f0ff5-108">Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration.</span></span><br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <span data-ttu-id="f0ff5-109"><dt>**WINBIO \_ DB \_ 啟動程式**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ff5-109"><dt>**WINBIO\_DB\_BOOTSTRAP**</dt></span></span> </dl> | <span data-ttu-id="f0ff5-110">可以用於啟動 Windows 之前的案例。</span><span class="sxs-lookup"><span data-stu-id="f0ff5-110">Can be used for scenarios prior to starting Windows.</span></span> <span data-ttu-id="f0ff5-111">一般而言，資料庫是感應器晶片的一部分或屬於 BIOS 的一部分，而且只能用於範本註冊與刪除。</span><span class="sxs-lookup"><span data-stu-id="f0ff5-111">Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.</span></span><br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <span data-ttu-id="f0ff5-112"><dt>**WINBIO \_ DB \_ ONCHIP**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ff5-112"><dt>**WINBIO\_DB\_ONCHIP**</dt></span></span> </dl>          | <span data-ttu-id="f0ff5-113">資料庫位於感應器晶片上。</span><span class="sxs-lookup"><span data-stu-id="f0ff5-113">The database resides on the sensor chip.</span></span><br/>                                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="f0ff5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0ff5-114">Requirements</span></span>



| <span data-ttu-id="f0ff5-115">需求</span><span class="sxs-lookup"><span data-stu-id="f0ff5-115">Requirement</span></span> | <span data-ttu-id="f0ff5-116">值</span><span class="sxs-lookup"><span data-stu-id="f0ff5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ff5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0ff5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ff5-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0ff5-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f0ff5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0ff5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ff5-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0ff5-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f0ff5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f0ff5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ff5-122"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f0ff5-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ff5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0ff5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ff5-124">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="f0ff5-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





