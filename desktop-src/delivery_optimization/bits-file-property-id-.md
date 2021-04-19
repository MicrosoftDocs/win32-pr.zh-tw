---
title: 'BITS_FILE_PROPERTY_ID 列舉 (>deliveryoptimization .h) '
description: BITS_FILE_PROPERTY_ID 列舉會指定定義對應至 BackgroundCopyFile 屬性之識別碼值的值。
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- BITS_FILE_PROPERTY_ID 列舉
- BITS_FILE_PROPERTY_ID 列舉
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968152"
---
# <a name="bits_file_property_id-enumeration"></a><span data-ttu-id="40c2a-105">BITS_FILE_PROPERTY_ID 列舉</span><span class="sxs-lookup"><span data-stu-id="40c2a-105">BITS_FILE_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="40c2a-106">**BITS_FILE_PROPERTY_ID** 列舉會指定定義對應至 **BACKGROUNDCOPYFILE** 屬性之識別碼值的值。</span><span class="sxs-lookup"><span data-stu-id="40c2a-106">The **BITS_FILE_PROPERTY_ID** enumeration specifies values that define ID values corresponding to **BackgroundCopyFile** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c2a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40c2a-107">Syntax</span></span>


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="40c2a-108">常數</span><span class="sxs-lookup"><span data-stu-id="40c2a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="40c2a-109"><span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**</span><span class="sxs-lookup"><span data-stu-id="40c2a-109"><span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**</span></span>
</dt> <dd>

<span data-ttu-id="40c2a-110">來自伺服器最後一個 HTTP 回應封包的一組完整 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="40c2a-110">The full set of HTTP response headers from the server's last HTTP response packet.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40c2a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="40c2a-111">Requirements</span></span>



| <span data-ttu-id="40c2a-112">需求</span><span class="sxs-lookup"><span data-stu-id="40c2a-112">Requirement</span></span> | <span data-ttu-id="40c2a-113">值</span><span class="sxs-lookup"><span data-stu-id="40c2a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c2a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40c2a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="40c2a-115">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40c2a-115">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="40c2a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40c2a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="40c2a-117">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40c2a-117">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="40c2a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="40c2a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="40c2a-119"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="40c2a-119"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





