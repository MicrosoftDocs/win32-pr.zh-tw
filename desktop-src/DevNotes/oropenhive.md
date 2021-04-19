---
description: 將指定的登錄 hive 檔案載入記憶體中，並驗證 hive。
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: 'OROpenHive 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984362"
---
# <a name="oropenhive-function"></a><span data-ttu-id="f835d-103">OROpenHive 函式</span><span class="sxs-lookup"><span data-stu-id="f835d-103">OROpenHive function</span></span>

<span data-ttu-id="f835d-104">將指定的登錄 hive 檔案載入記憶體中，並驗證 hive。</span><span class="sxs-lookup"><span data-stu-id="f835d-104">Loads the specified registry hive file into memory and validates the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="f835d-105">語法</span><span class="sxs-lookup"><span data-stu-id="f835d-105">Syntax</span></span>


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="f835d-106">參數</span><span class="sxs-lookup"><span data-stu-id="f835d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f835d-107">*lpHivePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f835d-107">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f835d-108">Unicode 字串的指標，指定要載入記憶體中的登錄 hive 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f835d-108">A pointer to a Unicode string that specifies the name of the registry hive file to be loaded into memory.</span></span> <span data-ttu-id="f835d-109">這可以是使用 [**ORSaveHive**](orsavehive.md) 函式所儲存或使用 [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) 或 [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) 函數所建立的 hive 檔案。</span><span class="sxs-lookup"><span data-stu-id="f835d-109">This can be a hive file that was saved with the [**ORSaveHive**](orsavehive.md) function or created with the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function.</span></span> <span data-ttu-id="f835d-110">檔案大小必須小於 4 GB，且呼叫端必須具有檔案 \_ 的檔案讀取 \_ 資料存取權。</span><span class="sxs-lookup"><span data-stu-id="f835d-110">The file must be less than 4 GB in size, and the caller must have FILE\_READ\_DATA access to the file.</span></span> <span data-ttu-id="f835d-111">如需詳細資訊，請參閱檔案 [安全性和存取權限](../fileio/file-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="f835d-111">For more information, see [File Security and Access Rights](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="f835d-112">*phkResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f835d-112">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f835d-113">變數的指標，此變數會接收已載入之離線登錄 hive 的根目錄控制碼。</span><span class="sxs-lookup"><span data-stu-id="f835d-113">A pointer to a variable that receives a handle to the root key of the loaded offline registry hive.</span></span> <span data-ttu-id="f835d-114">如果無法開啟登錄 hive 檔案或驗證失敗，函式會將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f835d-114">If the registry hive file cannot be opened or validation fails, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f835d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f835d-115">Return value</span></span>

<span data-ttu-id="f835d-116">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="f835d-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f835d-117">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f835d-117">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="f835d-118">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="f835d-118">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="f835d-119">可能的錯誤代碼包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="f835d-119">Possible error codes include the following:</span></span>

-   <span data-ttu-id="f835d-120">如果檔案大小為空白或大於 4 GB，則函式會傳回錯誤 \_ BADDB。</span><span class="sxs-lookup"><span data-stu-id="f835d-120">If the file is empty or larger than 4 GB in size, the function returns ERROR\_BADDB.</span></span>
-   <span data-ttu-id="f835d-121">如果呼叫端沒有開啟檔案的必要存取權限，則函式會傳回 \_ 拒絕存取錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f835d-121">If the caller does not have the necessary access rights to open the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="f835d-122">如果登錄 hive 驗證失敗，此函式會傳回錯誤，而不是登錄檔 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f835d-122">If the registry hive fails validation, the function returns ERROR\_NOT\_REGISTRY\_FILE.</span></span>

## <a name="remarks"></a><span data-ttu-id="f835d-123">備註</span><span class="sxs-lookup"><span data-stu-id="f835d-123">Remarks</span></span>

<span data-ttu-id="f835d-124">**OROpenHive** 函式是唯一可驗證登錄 hive 的離線登錄函式。</span><span class="sxs-lookup"><span data-stu-id="f835d-124">The **OROpenHive** function is the only offline registry function that validates a registry hive.</span></span> <span data-ttu-id="f835d-125">如果驗證失敗，則不會嘗試修復 hive。</span><span class="sxs-lookup"><span data-stu-id="f835d-125">If the validation fails, no attempt is made to repair the hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="f835d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f835d-126">Requirements</span></span>



| <span data-ttu-id="f835d-127">需求</span><span class="sxs-lookup"><span data-stu-id="f835d-127">Requirement</span></span> | <span data-ttu-id="f835d-128">值</span><span class="sxs-lookup"><span data-stu-id="f835d-128">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f835d-129">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f835d-129">Redistributable</span></span><br/> | <span data-ttu-id="f835d-130">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="f835d-130">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="f835d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f835d-131">Header</span></span><br/>          | <dl> <span data-ttu-id="f835d-132"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="f835d-132"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="f835d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f835d-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="f835d-134"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f835d-134"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f835d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f835d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f835d-136">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="f835d-136">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="f835d-137">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="f835d-137">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="f835d-138">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="f835d-138">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="f835d-139">RegSaveKey</span><span class="sxs-lookup"><span data-stu-id="f835d-139">RegSaveKey</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[<span data-ttu-id="f835d-140">RegSaveKeyEx</span><span class="sxs-lookup"><span data-stu-id="f835d-140">RegSaveKeyEx</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
