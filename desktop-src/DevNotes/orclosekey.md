---
description: 關閉離線登錄 hive 中指定之登錄機碼的控制碼。
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: 'ORCloseKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993621"
---
# <a name="orclosekey-function"></a><span data-ttu-id="0c24d-103">ORCloseKey 函式</span><span class="sxs-lookup"><span data-stu-id="0c24d-103">ORCloseKey function</span></span>

<span data-ttu-id="0c24d-104">關閉離線登錄 hive 中指定之登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0c24d-104">Closes a handle to the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c24d-105">語法</span><span class="sxs-lookup"><span data-stu-id="0c24d-105">Syntax</span></span>


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="0c24d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c24d-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c24d-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c24d-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0c24d-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c24d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c24d-109">Return value</span></span>

<span data-ttu-id="0c24d-110">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="0c24d-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0c24d-111">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0c24d-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="0c24d-112">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="0c24d-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="0c24d-113">如果指定的索引鍵是登錄區的根機碼，此函式會失敗，並出現錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="0c24d-113">If the specified key is the root key of the registry hive, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c24d-114">備註</span><span class="sxs-lookup"><span data-stu-id="0c24d-114">Remarks</span></span>

<span data-ttu-id="0c24d-115">指定之索引鍵的控制碼在關閉後不應使用，因為它將不再有效。</span><span class="sxs-lookup"><span data-stu-id="0c24d-115">The handle for a specified key should not be used after it has been closed, because it will no longer be valid.</span></span> <span data-ttu-id="0c24d-116">金鑰控制碼不應超過所需的時間保持開啟。</span><span class="sxs-lookup"><span data-stu-id="0c24d-116">Key handles should not be left open any longer than necessary.</span></span>

<span data-ttu-id="0c24d-117">使用 [**ORCloseHive**](orclosehive.md) 函式來關閉離線登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="0c24d-117">Use the [**ORCloseHive**](orclosehive.md) function to close an offline registry hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c24d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c24d-118">Requirements</span></span>



| <span data-ttu-id="0c24d-119">需求</span><span class="sxs-lookup"><span data-stu-id="0c24d-119">Requirement</span></span> | <span data-ttu-id="0c24d-120">值</span><span class="sxs-lookup"><span data-stu-id="0c24d-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c24d-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0c24d-121">Redistributable</span></span><br/> | <span data-ttu-id="0c24d-122">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="0c24d-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="0c24d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0c24d-123">Header</span></span><br/>          | <dl> <span data-ttu-id="0c24d-124"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c24d-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c24d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0c24d-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="0c24d-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c24d-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c24d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c24d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c24d-128">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="0c24d-128">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="0c24d-129">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="0c24d-129">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="0c24d-130">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="0c24d-130">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="0c24d-131">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="0c24d-131">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
