---
description: 開啟指定的磁片區，並初始化其配額控制物件。
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Initialize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971960"
---
# <a name="diskquotacontrolinitialize-method"></a><span data-ttu-id="a4a74-103">DiskQuotaControl.Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="a4a74-103">DiskQuotaControl.Initialize method</span></span>

<span data-ttu-id="a4a74-104">開啟指定的磁片區，並初始化其配額控制物件。</span><span class="sxs-lookup"><span data-stu-id="a4a74-104">Opens a specified volume and initializes its quota control object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a74-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4a74-105">Syntax</span></span>


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a><span data-ttu-id="a4a74-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4a74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a74-107">*sPath*</span><span class="sxs-lookup"><span data-stu-id="a4a74-107">*sPath*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a74-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4a74-108">Type: **String**</span></span>

<span data-ttu-id="a4a74-109">字串值，包含要初始化之磁片區的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a4a74-109">A string value that contains the fully qualified path of the volume to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="a4a74-110">*bReadWrite*</span><span class="sxs-lookup"><span data-stu-id="a4a74-110">*bReadWrite*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a74-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a4a74-111">Type: **Boolean**</span></span>

<span data-ttu-id="a4a74-112">指定如何開啟磁片區的布林值。</span><span class="sxs-lookup"><span data-stu-id="a4a74-112">A Boolean value that specifies how the volume is to be opened.</span></span> <span data-ttu-id="a4a74-113">將 *bReadWrite* 設為 **TRUE** 以進行讀取/寫入存取，或設定為 **FALSE** 表示唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="a4a74-113">Set *bReadWrite* to **TRUE** for read/write access or **FALSE** for read-only access.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4a74-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4a74-114">Return value</span></span>

<span data-ttu-id="a4a74-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a4a74-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a74-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4a74-116">Requirements</span></span>



| <span data-ttu-id="a4a74-117">需求</span><span class="sxs-lookup"><span data-stu-id="a4a74-117">Requirement</span></span> | <span data-ttu-id="a4a74-118">值</span><span class="sxs-lookup"><span data-stu-id="a4a74-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a74-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4a74-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a74-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4a74-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4a74-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4a74-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a74-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4a74-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a4a74-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a74-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4a74-124"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a4a74-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a74-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4a74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a74-126">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="a4a74-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




