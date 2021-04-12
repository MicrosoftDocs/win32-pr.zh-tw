---
description: 包含 IP 或 IPX 通訊協定所使用的埠號碼。
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: 'GENERIC_PORT 聯集 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936631"
---
# <a name="generic_port-union"></a><span data-ttu-id="a0189-103">泛型 \_ 埠聯集</span><span class="sxs-lookup"><span data-stu-id="a0189-103">GENERIC\_PORT union</span></span>

<span data-ttu-id="a0189-104">**一般 \_ 埠** 結構包含 IP 或 IPX 通訊協定所使用的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a0189-104">The **GENERIC\_PORT** structure contains a port number used for IP or IPX protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0189-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0189-105">Syntax</span></span>


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a><span data-ttu-id="a0189-106">成員</span><span class="sxs-lookup"><span data-stu-id="a0189-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0189-107">**IPPort**</span><span class="sxs-lookup"><span data-stu-id="a0189-107">**IPPort**</span></span>
</dt> <dd>

<span data-ttu-id="a0189-108">填入的 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a0189-108">IP port number filled in.</span></span>

</dd> <dt>

<span data-ttu-id="a0189-109">**ByteSwappedIPXPort**</span><span class="sxs-lookup"><span data-stu-id="a0189-109">**ByteSwappedIPXPort**</span></span>
</dt> <dd>

<span data-ttu-id="a0189-110">填入的 IPX 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a0189-110">IPX port number filled in.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0189-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0189-111">Requirements</span></span>



| <span data-ttu-id="a0189-112">需求</span><span class="sxs-lookup"><span data-stu-id="a0189-112">Requirement</span></span> | <span data-ttu-id="a0189-113">值</span><span class="sxs-lookup"><span data-stu-id="a0189-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0189-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0189-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a0189-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0189-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0189-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0189-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a0189-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0189-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a0189-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a0189-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0189-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a0189-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




