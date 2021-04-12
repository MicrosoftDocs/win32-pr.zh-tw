---
description: 儲存無線設定服務所管理的無線區域網路介面相關的重要資訊。
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: 'INTF_KEY_ENTRY 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318535"
---
# <a name="intf_key_entry-structure"></a><span data-ttu-id="2a1c9-103">INTF \_ \_ 索引鍵輸入結構</span><span class="sxs-lookup"><span data-stu-id="2a1c9-103">INTF\_KEY\_ENTRY structure</span></span>

<span data-ttu-id="2a1c9-104">\[**INTF \_Windows \_** Vista 和 windows Server 2008 不再支援金鑰輸入。</span><span class="sxs-lookup"><span data-stu-id="2a1c9-104">\[**INTF\_KEY\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="2a1c9-105">相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="2a1c9-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="2a1c9-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="2a1c9-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="2a1c9-107">**INTF 機 \_ 碼 \_ 輸入** 結構會儲存無線設定服務所管理的無線區域網路介面相關的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="2a1c9-107">The **INTF\_KEY\_ENTRY** structure stores the key information about a wireless LAN interface managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1c9-108">語法</span><span class="sxs-lookup"><span data-stu-id="2a1c9-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a><span data-ttu-id="2a1c9-109">成員</span><span class="sxs-lookup"><span data-stu-id="2a1c9-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a1c9-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="2a1c9-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="2a1c9-111">以下列格式的 Unicode 字串形式表示之介面 GUID 的指標： "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"。</span><span class="sxs-lookup"><span data-stu-id="2a1c9-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a1c9-112">備註</span><span class="sxs-lookup"><span data-stu-id="2a1c9-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2a1c9-113">Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="2a1c9-113">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a1c9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a1c9-114">Requirements</span></span>



| <span data-ttu-id="2a1c9-115">需求</span><span class="sxs-lookup"><span data-stu-id="2a1c9-115">Requirement</span></span> | <span data-ttu-id="2a1c9-116">值</span><span class="sxs-lookup"><span data-stu-id="2a1c9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1c9-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a1c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a1c9-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a1c9-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a1c9-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a1c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a1c9-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a1c9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a1c9-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2a1c9-121">End of client support</span></span><br/>    | <span data-ttu-id="2a1c9-122">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="2a1c9-122">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="2a1c9-123">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2a1c9-123">End of server support</span></span><br/>    | <span data-ttu-id="2a1c9-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a1c9-124">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="2a1c9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2a1c9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a1c9-126"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a1c9-126"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a1c9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a1c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1c9-128">**INTFS 索引 \_ 鍵 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="2a1c9-128">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="2a1c9-129">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="2a1c9-129">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> </dl>

 

 




