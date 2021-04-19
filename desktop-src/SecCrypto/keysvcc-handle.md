---
description: KEYSVCC \_ 控制碼資料類型會定義金鑰服務控制碼。 \_RKeyOpenKeyService 和 RKeyCloseKeyService 函數會使用 KEYSVCC 控制碼控制碼。
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: 'KEYSVCC_HANDLE (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1427a4ffd4637e073e517e5df54af72191992d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983834"
---
# <a name="keysvcc_handle"></a><span data-ttu-id="5c971-104">KEYSVCC \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="5c971-104">KEYSVCC\_HANDLE</span></span>

<span data-ttu-id="5c971-105">**KEYSVCC \_ 控制碼** 資料類型會定義金鑰服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="5c971-105">The **KEYSVCC\_HANDLE** data type defines a key service handle.</span></span> <span data-ttu-id="5c971-106">[**RKeyOpenKeyService**](rkeyopenkeyservice.md)和 [**RKeyCloseKeyService**](rkeyclosekeyservice.md)函數會使用 **KEYSVCC \_ 句** 柄控制碼。</span><span class="sxs-lookup"><span data-stu-id="5c971-106">A **KEYSVCC\_HANDLE** handle is used by the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) and [**RKeyCloseKeyService**](rkeyclosekeyservice.md) functions.</span></span>


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="5c971-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c971-107">Requirements</span></span>



| <span data-ttu-id="5c971-108">需求</span><span class="sxs-lookup"><span data-stu-id="5c971-108">Requirement</span></span> | <span data-ttu-id="5c971-109">值</span><span class="sxs-lookup"><span data-stu-id="5c971-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c971-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c971-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5c971-111">都不支援</span><span class="sxs-lookup"><span data-stu-id="5c971-111">None supported</span></span><br/>                                                             |
| <span data-ttu-id="5c971-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c971-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5c971-113">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c971-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c971-114">標頭</span><span class="sxs-lookup"><span data-stu-id="5c971-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c971-115"><dt>Rkeysvcc。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c971-115"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c971-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c971-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c971-117">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="5c971-117">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="5c971-118">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="5c971-118">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




