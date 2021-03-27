---
description: 用來指定登錄中安全性存取屬性的資料類型。
title: 'REGSAM (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974916"
---
# <a name="regsam"></a><span data-ttu-id="edde7-103">REGSAM</span><span class="sxs-lookup"><span data-stu-id="edde7-103">REGSAM</span></span>

<span data-ttu-id="edde7-104">用來指定登錄中安全性存取屬性的資料類型。</span><span class="sxs-lookup"><span data-stu-id="edde7-104">A data type used for specifying the security access attributes in the registry.</span></span>



| <span data-ttu-id="edde7-105">常數</span><span class="sxs-lookup"><span data-stu-id="edde7-105">Constant</span></span>                                                                                                                                                                                   | <span data-ttu-id="edde7-106">描述</span><span class="sxs-lookup"><span data-stu-id="edde7-106">Description</span></span>                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <span data-ttu-id="edde7-107"><dt>**金鑰 \_ 所有 \_ 存取權**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-107"><dt>**KEY\_ALL\_ACCESS**</dt></span></span> </dl>                          | <span data-ttu-id="edde7-108">\* \* \* \* 索引鍵 \_ 查詢值 \* \* \* *、* \* \* \* 金鑰列舉子機碼 \* \* \* *、* \* \* \* 金鑰通知 \* \* \* *、* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* 金鑰建立連結 \* \* \* \* \_ \_ 和 \* \* \* \_ \_ \_ \_ \_ \_ \_ \_ \* 金鑰 \_ 集 \_ 值 \* \* \* \* 存取的組合。</span><span class="sxs-lookup"><span data-stu-id="edde7-108">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, \*\*\*\*KEY\_NOTIFY\*\*\*\*, \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\*, \*\*\*\*KEY\_CREATE\_LINK\*\*\*\*, and \*\*\*\*KEY\_SET\_VALUE\*\*\*\* access.</span></span><br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <span data-ttu-id="edde7-109"><dt>**金鑰 \_ 建立 \_ 連結**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-109"><dt>**KEY\_CREATE\_LINK**</dt></span></span> </dl>                       | <span data-ttu-id="edde7-110">建立符號連結的許可權。</span><span class="sxs-lookup"><span data-stu-id="edde7-110">Permission to create a symbolic link.</span></span><br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <span data-ttu-id="edde7-111"><dt>**金鑰 \_ 建立 \_ 子機 \_ 碼**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-111"><dt>**KEY\_CREATE\_SUB\_KEY**</dt></span></span> </dl>             | <span data-ttu-id="edde7-112">建立子機碼的許可權。</span><span class="sxs-lookup"><span data-stu-id="edde7-112">Permission to create subkeys.</span></span><br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <span data-ttu-id="edde7-113"><dt>**金鑰 \_ 列舉 \_ 子 \_ 機碼**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-113"><dt>**KEY\_ENUMERATE\_SUB\_KEYS**</dt></span></span> </dl> | <span data-ttu-id="edde7-114">列舉子機碼的許可權。</span><span class="sxs-lookup"><span data-stu-id="edde7-114">Permission to enumerate subkeys.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <span data-ttu-id="edde7-115"><dt>**金鑰 \_ 執行**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-115"><dt>**KEY\_EXECUTE**</dt></span></span> </dl>                                    | <span data-ttu-id="edde7-116">讀取權限的許可權。</span><span class="sxs-lookup"><span data-stu-id="edde7-116">Permission for read access.</span></span><br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <span data-ttu-id="edde7-117"><dt>**金鑰 \_ 通知**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-117"><dt>**KEY\_NOTIFY**</dt></span></span> </dl>                                       | <span data-ttu-id="edde7-118">變更通知的許可權。</span><span class="sxs-lookup"><span data-stu-id="edde7-118">Permission for change notification.</span></span><br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <span data-ttu-id="edde7-119"><dt>**金鑰 \_ 查詢 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-119"><dt>**KEY\_QUERY\_VALUE**</dt></span></span> </dl>                       | <span data-ttu-id="edde7-120">查詢子機碼資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="edde7-120">Permission to query subkey data.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <span data-ttu-id="edde7-121"><dt>**金鑰 \_ 讀取**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-121"><dt>**KEY\_READ**</dt></span></span> </dl>                                             | <span data-ttu-id="edde7-122">\* \* \* \* 索引鍵 \_ 查詢 \_ 值 \* \* \* *、* \* \* \* 金鑰 \_ 列舉子機碼 \* \* \* \* 和 \* \* \* \_ \_ \* 金鑰 \_ 通知 \* \* \* \* 存取的組合。</span><span class="sxs-lookup"><span data-stu-id="edde7-122">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, and \*\*\*\*KEY\_NOTIFY\*\*\*\* access.</span></span><br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <span data-ttu-id="edde7-123"><dt>**索引鍵 \_ 集 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-123"><dt>**KEY\_SET\_VALUE**</dt></span></span> </dl>                             | <span data-ttu-id="edde7-124">設定子機碼資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="edde7-124">Permission to set subkey data.</span></span><br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <span data-ttu-id="edde7-125"><dt>**金鑰 \_ 寫入**</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-125"><dt>**KEY\_WRITE**</dt></span></span> </dl>                                          | <span data-ttu-id="edde7-126">\* \* \* \* KEY \_ SET \_ VALUE \* \* \* \* 和 \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="edde7-126">Combination of \*\*\*\*KEY\_SET\_VALUE\*\*\*\* and \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\* access.</span></span><br/>                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="edde7-127">備註</span><span class="sxs-lookup"><span data-stu-id="edde7-127">Remarks</span></span>

<span data-ttu-id="edde7-128">**REGSAM** 值可以是一個或多個列出的值。</span><span class="sxs-lookup"><span data-stu-id="edde7-128">A **REGSAM** value can be one or more of the listed values.</span></span>

## <a name="requirements"></a><span data-ttu-id="edde7-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="edde7-129">Requirements</span></span>



| <span data-ttu-id="edde7-130">需求</span><span class="sxs-lookup"><span data-stu-id="edde7-130">Requirement</span></span> | <span data-ttu-id="edde7-131">值</span><span class="sxs-lookup"><span data-stu-id="edde7-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="edde7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="edde7-132">Header</span></span><br/> | <dl> <span data-ttu-id="edde7-133"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="edde7-133"><dt>Winnt.h</dt></span></span> </dl> |



 

 




