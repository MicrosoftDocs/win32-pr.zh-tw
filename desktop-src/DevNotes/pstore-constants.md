---
description: PStore 會使用下列常數。
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: 'PStore 常數 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994090"
---
# <a name="pstore-constants"></a><span data-ttu-id="d09bc-103">PStore 常數</span><span class="sxs-lookup"><span data-stu-id="d09bc-103">PStore Constants</span></span>

<span data-ttu-id="d09bc-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d09bc-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d09bc-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="d09bc-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d09bc-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="d09bc-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d09bc-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="d09bc-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d09bc-108">PStore 會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="d09bc-108">The following constants are used by PStore.</span></span>

<span data-ttu-id="d09bc-109">受保護的儲存體錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d09bc-109">Protected Storage Error Codes</span></span>



| <span data-ttu-id="d09bc-110">常數/值</span><span class="sxs-lookup"><span data-stu-id="d09bc-110">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="d09bc-111">Description</span><span class="sxs-lookup"><span data-stu-id="d09bc-111">Description</span></span>                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <span data-ttu-id="d09bc-112"><dt>**PST \_E \_ OK**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="d09bc-112"><dt>**PST\_E\_OK**</dt> <dt>0x00000000L</dt></span></span> </dl>                             | <span data-ttu-id="d09bc-113">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d09bc-113">The operation was successful.</span></span><br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <span data-ttu-id="d09bc-114"><dt>**PST \_E \_ 類型 \_ 存在**</dt> <dt>0x800C0004L</dt></span><span class="sxs-lookup"><span data-stu-id="d09bc-114"><dt>**PST\_E\_TYPE\_EXISTS**</dt> <dt>0x800C0004L</dt></span></span> </dl> | <span data-ttu-id="d09bc-115">資料項目目已存在於受保護的儲存體中。</span><span class="sxs-lookup"><span data-stu-id="d09bc-115">The data item already exists in the protected storage.</span></span> <br/> |



<span data-ttu-id="d09bc-116">存取子句值</span><span class="sxs-lookup"><span data-stu-id="d09bc-116">Access Clause Values</span></span>



| <span data-ttu-id="d09bc-117">常數/值</span><span class="sxs-lookup"><span data-stu-id="d09bc-117">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="d09bc-118">Description</span><span class="sxs-lookup"><span data-stu-id="d09bc-118">Description</span></span>                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <span data-ttu-id="d09bc-119"><dt>**PST \_AUTHENTICODE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d09bc-119"><dt>**PST\_AUTHENTICODE**</dt> <dt>1</dt></span></span> </dl>                       | <span data-ttu-id="d09bc-120">指向 [**PST \_ AUTHENTICODEDATA**](pst-authenticodedata.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d09bc-120">Points to a [**PST\_AUTHENTICODEDATA**](pst-authenticodedata.md) structure.</span></span><br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <span data-ttu-id="d09bc-121"><dt> **PST \_ 二進位 \_ 檢查**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d09bc-121"><dt>**PST\_BINARY\_CHECK** </dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="d09bc-122">指向 **PST \_ BINARYCHECKDATA** 結構。</span><span class="sxs-lookup"><span data-stu-id="d09bc-122">Points to a **PST\_BINARYCHECKDATA** structure.</span></span><br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <span data-ttu-id="d09bc-123"><dt>**PST \_安全 \_ 描述項**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d09bc-123"><dt>**PST\_SECURITY\_DESCRIPTOR**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="d09bc-124">指向有效的 Windows 安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d09bc-124">Points to a valid Windows security descriptor.</span></span> <br/>                              |



## <a name="requirements"></a><span data-ttu-id="d09bc-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d09bc-125">Requirements</span></span>



| <span data-ttu-id="d09bc-126">需求</span><span class="sxs-lookup"><span data-stu-id="d09bc-126">Requirement</span></span> | <span data-ttu-id="d09bc-127">值</span><span class="sxs-lookup"><span data-stu-id="d09bc-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d09bc-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d09bc-128">Header</span></span><br/> | <dl> <span data-ttu-id="d09bc-129"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="d09bc-129"><dt>Pstore.h</dt></span></span> </dl> |



 

 
