---
description: 建立包含單一空根金鑰的離線登錄 hive。
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: 'ORCreateHive 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987914"
---
# <a name="orcreatehive-function"></a><span data-ttu-id="96c48-103">ORCreateHive 函式</span><span class="sxs-lookup"><span data-stu-id="96c48-103">ORCreateHive function</span></span>

<span data-ttu-id="96c48-104">建立包含單一空根金鑰的離線登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="96c48-104">Creates an offline registry hive that contains a single empty root key.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c48-105">語法</span><span class="sxs-lookup"><span data-stu-id="96c48-105">Syntax</span></span>


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="96c48-106">參數</span><span class="sxs-lookup"><span data-stu-id="96c48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c48-107">*phkResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="96c48-107">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96c48-108">指向變數，以接收新建立之離線登錄 hive 的根目錄控制碼。</span><span class="sxs-lookup"><span data-stu-id="96c48-108">Points to a variable to receive a handle to the root key of the newly created offline registry hive.</span></span> <span data-ttu-id="96c48-109">如果無法建立 hive，此函式會將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="96c48-109">If the hive cannot be created, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c48-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="96c48-110">Return value</span></span>

<span data-ttu-id="96c48-111">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="96c48-111">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="96c48-112">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="96c48-112">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="96c48-113">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="96c48-113">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="96c48-114">如果記憶體不足，無法建立登錄區，則函式會傳回錯誤 \_ 的 \_ \_ 記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="96c48-114">If there is insufficient memory to create the registry hive, the function returns ERROR\_NOT\_ENOUGH\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="96c48-115">備註</span><span class="sxs-lookup"><span data-stu-id="96c48-115">Remarks</span></span>

<span data-ttu-id="96c48-116">**ORCreateHive** 函式會在記憶體中建立空白的離線登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="96c48-116">The **ORCreateHive** function creates an empty offline registry hive in memory.</span></span> <span data-ttu-id="96c48-117">使用 [**ORCreateKey**](orcreatekey.md) 和 [**ORSetValue**](orsetvalue.md) 函式來新增索引鍵並設定其值。</span><span class="sxs-lookup"><span data-stu-id="96c48-117">Use the [**ORCreateKey**](orcreatekey.md) and [**ORSetValue**](orsetvalue.md) functions to add keys and set their values.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c48-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="96c48-118">Requirements</span></span>



| <span data-ttu-id="96c48-119">需求</span><span class="sxs-lookup"><span data-stu-id="96c48-119">Requirement</span></span> | <span data-ttu-id="96c48-120">值</span><span class="sxs-lookup"><span data-stu-id="96c48-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96c48-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="96c48-121">Redistributable</span></span><br/> | <span data-ttu-id="96c48-122">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="96c48-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="96c48-123">標頭</span><span class="sxs-lookup"><span data-stu-id="96c48-123">Header</span></span><br/>          | <dl> <span data-ttu-id="96c48-124"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="96c48-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="96c48-125">DLL</span><span class="sxs-lookup"><span data-stu-id="96c48-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="96c48-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96c48-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c48-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96c48-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c48-128">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="96c48-128">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="96c48-129">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="96c48-129">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="96c48-130">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="96c48-130">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="96c48-131">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="96c48-131">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
