---
description: 啟用或停用磁片磁區的讀取和寫入。
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847183"
---
# <a name="fveenablerawaccessw-function"></a><span data-ttu-id="748c2-103">FveEnableRawAccessW 函式</span><span class="sxs-lookup"><span data-stu-id="748c2-103">FveEnableRawAccessW function</span></span>

<span data-ttu-id="748c2-104">啟用或停用磁片磁區的讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="748c2-104">Enables or disables reading and writing of disk sectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="748c2-105">語法</span><span class="sxs-lookup"><span data-stu-id="748c2-105">Syntax</span></span>


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="748c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="748c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="748c2-107">*VolumeName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="748c2-107">*VolumeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="748c2-108">磁片區的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="748c2-108">A unique identifier for the disk volume.</span></span>

</dd> <dt>

<span data-ttu-id="748c2-109">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="748c2-109">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="748c2-110">若 **為 TRUE**，則允許存取原始磁片區。</span><span class="sxs-lookup"><span data-stu-id="748c2-110">If **TRUE**, allows access to the raw volume.</span></span> <span data-ttu-id="748c2-111">如果 **為 FALSE**，則不允許對未經處理的磁片區進行存取。</span><span class="sxs-lookup"><span data-stu-id="748c2-111">If **FALSE**, no access is allowed to the raw volume.</span></span> <span data-ttu-id="748c2-112">如果已啟用原始存取，但此值為 **FALSE**，則磁片區會重新掛接和重新驗證。</span><span class="sxs-lookup"><span data-stu-id="748c2-112">If raw access has already been enabled but this value is **FALSE**, the volume is remounted and revalidated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="748c2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="748c2-113">Return value</span></span>

<span data-ttu-id="748c2-114">此函式會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="748c2-114">This function returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="748c2-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="748c2-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="748c2-116">Description</span><span class="sxs-lookup"><span data-stu-id="748c2-116">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="748c2-117"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="748c2-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                           | <span data-ttu-id="748c2-118">函數成功。</span><span class="sxs-lookup"><span data-stu-id="748c2-118">The function was successful.</span></span><br/>                                            |
| <dl> <span data-ttu-id="748c2-119"><dt>**S \_FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="748c2-119"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                        | <span data-ttu-id="748c2-120">Enabled 為 **FALSE** ，且磁片區尚未處於原始存取模式。</span><span class="sxs-lookup"><span data-stu-id="748c2-120">Enabled is **FALSE** and the volume was not already in raw access mode.</span></span><br/> |
| <dl> <span data-ttu-id="748c2-121"><dt>**E \_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="748c2-121"><dt>**E\_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl> | <span data-ttu-id="748c2-122">無法鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="748c2-122">The volume cannot be locked.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="748c2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="748c2-123">Requirements</span></span>



| <span data-ttu-id="748c2-124">需求</span><span class="sxs-lookup"><span data-stu-id="748c2-124">Requirement</span></span> | <span data-ttu-id="748c2-125">值</span><span class="sxs-lookup"><span data-stu-id="748c2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="748c2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="748c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="748c2-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="748c2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="748c2-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="748c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="748c2-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="748c2-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="748c2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="748c2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="748c2-131"><dt>Fveapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="748c2-131"><dt>Fveapi.dll</dt></span></span> </dl> |



 

 




