---
description: PROTOCOLINFO 結構描述通訊協定。
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: 'PROTOCOLINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996863"
---
# <a name="protocolinfo-structure"></a><span data-ttu-id="f50da-103">PROTOCOLINFO 結構</span><span class="sxs-lookup"><span data-stu-id="f50da-103">PROTOCOLINFO structure</span></span>

<span data-ttu-id="f50da-104">**PROTOCOLINFO** 結構描述通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f50da-104">The **PROTOCOLINFO** structure describes a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="f50da-105">語法</span><span class="sxs-lookup"><span data-stu-id="f50da-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a><span data-ttu-id="f50da-106">成員</span><span class="sxs-lookup"><span data-stu-id="f50da-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f50da-107">**ProtocolID**</span><span class="sxs-lookup"><span data-stu-id="f50da-107">**ProtocolID**</span></span>
</dt> <dd>

<span data-ttu-id="f50da-108">指定之執行會話的系統指派通訊協定識別碼。</span><span class="sxs-lookup"><span data-stu-id="f50da-108">System-assigned protocol identifier of the specified run session.</span></span>

</dd> <dt>

<span data-ttu-id="f50da-109">**PropertyDatabase**</span><span class="sxs-lookup"><span data-stu-id="f50da-109">**PropertyDatabase**</span></span>
</dt> <dd>

<span data-ttu-id="f50da-110">指定之通訊協定的屬性資料庫。</span><span class="sxs-lookup"><span data-stu-id="f50da-110">Property database of the specified protocol.</span></span>

</dd> <dt>

<span data-ttu-id="f50da-111">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="f50da-111">**ProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="f50da-112">縮寫的通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="f50da-112">Abbreviated protocol name.</span></span>

</dd> <dt>

<span data-ttu-id="f50da-113">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="f50da-113">**HelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="f50da-114">與通訊協定相關聯的選擇性說明檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f50da-114">Optional Help file name associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="f50da-115">**註解**</span><span class="sxs-lookup"><span data-stu-id="f50da-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="f50da-116">描述通訊協定的批註。</span><span class="sxs-lookup"><span data-stu-id="f50da-116">A comment describing the protocol.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f50da-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f50da-117">Requirements</span></span>



| <span data-ttu-id="f50da-118">需求</span><span class="sxs-lookup"><span data-stu-id="f50da-118">Requirement</span></span> | <span data-ttu-id="f50da-119">值</span><span class="sxs-lookup"><span data-stu-id="f50da-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f50da-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f50da-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f50da-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f50da-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f50da-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f50da-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f50da-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f50da-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f50da-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f50da-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f50da-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f50da-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




