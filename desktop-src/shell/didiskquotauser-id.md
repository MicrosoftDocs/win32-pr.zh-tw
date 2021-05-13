---
description: 取得可唯一識別使用者的識別碼。
title: DIDiskQuotaUser.ID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.ID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5cf2610e-fbd2-4e87-a323-f024283db546
ms.openlocfilehash: 389c07325f4e504424c43b0983eaa643ea608008
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841610"
---
# <a name="didiskquotauserid-property"></a><span data-ttu-id="2b12a-103">DIDiskQuotaUser.ID 屬性</span><span class="sxs-lookup"><span data-stu-id="2b12a-103">DIDiskQuotaUser.ID property</span></span>

<span data-ttu-id="2b12a-104">取得可唯一識別使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b12a-104">Gets an ID that uniquely identifies the user.</span></span>

<span data-ttu-id="2b12a-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2b12a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b12a-106">語法</span><span class="sxs-lookup"><span data-stu-id="2b12a-106">Syntax</span></span>


```JScript
iID = DIDiskQuotaUser.ID
```



## <a name="property-value"></a><span data-ttu-id="2b12a-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="2b12a-107">Property value</span></span>

<span data-ttu-id="2b12a-108">**整數** 值，可在特定 [**DiskQuotaControl**](diskquotacontrol-object.md)進程內唯一識別使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="2b12a-108">An **Integer** value that uniquely identifies the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object within a particular [**DiskQuotaControl**](diskquotacontrol-object.md) process.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b12a-109">備註</span><span class="sxs-lookup"><span data-stu-id="2b12a-109">Remarks</span></span>

<span data-ttu-id="2b12a-110">這個屬性是供不支援指標的語言（例如 Microsoft Visual Basic）使用。</span><span class="sxs-lookup"><span data-stu-id="2b12a-110">This property is intended for use by languages such as Microsoft Visual Basic that do not support pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b12a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b12a-111">Requirements</span></span>



| <span data-ttu-id="2b12a-112">需求</span><span class="sxs-lookup"><span data-stu-id="2b12a-112">Requirement</span></span> | <span data-ttu-id="2b12a-113">值</span><span class="sxs-lookup"><span data-stu-id="2b12a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b12a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b12a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2b12a-115">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b12a-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b12a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b12a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2b12a-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b12a-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2b12a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="2b12a-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b12a-119"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2b12a-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b12a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b12a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b12a-121">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="2b12a-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




