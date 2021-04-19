---
title: 'WM_BACKUP_RESTORE_STATUS 結構 (Wmdrmsdk .h) '
description: WM \_ 備份 \_ 還原 \_ 狀態結構會保存有關暫止授權備份或還原作業的資訊。
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- WM_BACKUP_RESTORE_STATUS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995416"
---
# <a name="wm_backup_restore_status-structure"></a><span data-ttu-id="dde4b-105">WM \_ 備份 \_ 還原 \_ 狀態結構</span><span class="sxs-lookup"><span data-stu-id="dde4b-105">WM\_BACKUP\_RESTORE\_STATUS structure</span></span>

<span data-ttu-id="dde4b-106">**WM \_ 備份 \_ 還原 \_ 狀態** 結構會保存有關暫止授權備份或還原作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="dde4b-106">The **WM\_BACKUP\_RESTORE\_STATUS** structure holds information about a pending license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde4b-107">語法</span><span class="sxs-lookup"><span data-stu-id="dde4b-107">Syntax</span></span>


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a><span data-ttu-id="dde4b-108">成員</span><span class="sxs-lookup"><span data-stu-id="dde4b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dde4b-109">**eStatus**</span><span class="sxs-lookup"><span data-stu-id="dde4b-109">**eStatus**</span></span>
</dt> <dd>

<span data-ttu-id="dde4b-110">[**MSDRM \_ 狀態**](msdrm-status.md)列舉的成員，指定狀態。</span><span class="sxs-lookup"><span data-stu-id="dde4b-110">Member of the [**MSDRM\_STATUS**](msdrm-status.md) enumeration specifying the status.</span></span>

</dd> <dt>

<span data-ttu-id="dde4b-111">**bstrError**</span><span class="sxs-lookup"><span data-stu-id="dde4b-111">**bstrError**</span></span>
</dt> <dd>

<span data-ttu-id="dde4b-112">包含錯誤的字串。</span><span class="sxs-lookup"><span data-stu-id="dde4b-112">String containing the error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dde4b-113">備註</span><span class="sxs-lookup"><span data-stu-id="dde4b-113">Remarks</span></span>

<span data-ttu-id="dde4b-114">當您呼叫 [**IWMDRMLicenseBackupRestoreStatus：： GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) 方法時，就會收到此結構。</span><span class="sxs-lookup"><span data-stu-id="dde4b-114">This structure is received when you call the [**IWMDRMLicenseBackupRestoreStatus::GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) method.</span></span> <span data-ttu-id="dde4b-115">它包含在呼叫時暫止的備份或還原作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="dde4b-115">It contains the status of the pending backup or restore operation at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde4b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dde4b-116">Requirements</span></span>



| <span data-ttu-id="dde4b-117">需求</span><span class="sxs-lookup"><span data-stu-id="dde4b-117">Requirement</span></span> | <span data-ttu-id="dde4b-118">值</span><span class="sxs-lookup"><span data-stu-id="dde4b-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dde4b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="dde4b-119">Header</span></span><br/> | <dl> <span data-ttu-id="dde4b-120"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="dde4b-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde4b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dde4b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde4b-122">**結構**</span><span class="sxs-lookup"><span data-stu-id="dde4b-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





