---
description: IPX \_ 位址結構會提供 ipx 通訊協定層級的位址。
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: 'IPX_ADDRESS 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511240"
---
# <a name="ipx_address-structure"></a><span data-ttu-id="27ae2-103">IPX \_ 位址結構</span><span class="sxs-lookup"><span data-stu-id="27ae2-103">IPX\_ADDRESS structure</span></span>

<span data-ttu-id="27ae2-104">**Ipx \_ 位址** 結構會提供 ipx 通訊協定層級的位址。</span><span class="sxs-lookup"><span data-stu-id="27ae2-104">The **IPX\_ADDRESS** structure provides an address at the IPX protocol level.</span></span>

## <a name="syntax"></a><span data-ttu-id="27ae2-105">語法</span><span class="sxs-lookup"><span data-stu-id="27ae2-105">Syntax</span></span>


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="27ae2-106">成員</span><span class="sxs-lookup"><span data-stu-id="27ae2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="27ae2-107">**子網路**</span><span class="sxs-lookup"><span data-stu-id="27ae2-107">**Subnet**</span></span>
</dt> <dd>

<span data-ttu-id="27ae2-108">網路子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="27ae2-108">Network subnet identifier.</span></span>

</dd> <dt>

<span data-ttu-id="27ae2-109">**位址**</span><span class="sxs-lookup"><span data-stu-id="27ae2-109">**Address**</span></span>
</dt> <dd>

<span data-ttu-id="27ae2-110">子網 NIC 識別碼。</span><span class="sxs-lookup"><span data-stu-id="27ae2-110">Subnet NIC identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27ae2-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="27ae2-111">Requirements</span></span>



| <span data-ttu-id="27ae2-112">需求</span><span class="sxs-lookup"><span data-stu-id="27ae2-112">Requirement</span></span> | <span data-ttu-id="27ae2-113">值</span><span class="sxs-lookup"><span data-stu-id="27ae2-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="27ae2-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27ae2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="27ae2-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27ae2-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="27ae2-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27ae2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="27ae2-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27ae2-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="27ae2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="27ae2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="27ae2-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="27ae2-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




