---
description: 關閉指定的離線登錄 hive，並釋出配置給 hive 的記憶體。
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: 'ORCloseHive 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979543"
---
# <a name="orclosehive-function"></a><span data-ttu-id="8fb31-103">ORCloseHive 函式</span><span class="sxs-lookup"><span data-stu-id="8fb31-103">ORCloseHive function</span></span>

<span data-ttu-id="8fb31-104">關閉指定的離線登錄 hive，並釋出配置給 hive 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8fb31-104">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb31-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fb31-105">Syntax</span></span>


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="8fb31-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fb31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb31-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fb31-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb31-108">要關閉之離線登錄 hive 的根目錄控制碼。</span><span class="sxs-lookup"><span data-stu-id="8fb31-108">A handle to the root key of the offline registry hive to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb31-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fb31-109">Return value</span></span>

<span data-ttu-id="8fb31-110">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="8fb31-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8fb31-111">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8fb31-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="8fb31-112">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="8fb31-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb31-113">備註</span><span class="sxs-lookup"><span data-stu-id="8fb31-113">Remarks</span></span>

<span data-ttu-id="8fb31-114">**ORCloseHive** 函式會代表指定的 hive 釋出離線登錄功能所配置的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="8fb31-114">The **ORCloseHive** function frees all memory allocated by the offline registry functions on behalf of the specified hive.</span></span>

<span data-ttu-id="8fb31-115">若要保留對 hive 的變更，請在呼叫 **ORCloseHive** 之前呼叫 [**ORSaveHive**](orsavehive.md)函數。</span><span class="sxs-lookup"><span data-stu-id="8fb31-115">To preserve changes to the hive, call the [**ORSaveHive**](orsavehive.md) function before calling **ORCloseHive**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb31-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fb31-116">Requirements</span></span>



| <span data-ttu-id="8fb31-117">需求</span><span class="sxs-lookup"><span data-stu-id="8fb31-117">Requirement</span></span> | <span data-ttu-id="8fb31-118">值</span><span class="sxs-lookup"><span data-stu-id="8fb31-118">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb31-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8fb31-119">Redistributable</span></span><br/> | <span data-ttu-id="8fb31-120">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8fb31-120">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="8fb31-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8fb31-121">Header</span></span><br/>          | <dl> <span data-ttu-id="8fb31-122"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb31-122"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fb31-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8fb31-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="8fb31-124"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fb31-124"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb31-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fb31-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb31-126">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="8fb31-126">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="8fb31-127">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="8fb31-127">**ORSaveHive**</span></span>](orsavehive.md)
</dt> </dl>

 

 
