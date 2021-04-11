---
title: 'MCI_OPEN_PARMS 結構 (Mciapi .h) '
description: MCI \_ open \_ PARMS 結構包含 mci open 命令的資訊 \_ 。
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094391"
---
# <a name="mci_open_parms-structure"></a><span data-ttu-id="a5c43-104">MCI \_ 開啟 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="a5c43-104">MCI\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="a5c43-105">**Mci \_ open \_ PARMS** 結構包含 [**mci \_ open**](mci-open.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="a5c43-105">The **MCI\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c43-106">語法</span><span class="sxs-lookup"><span data-stu-id="a5c43-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="a5c43-107">成員</span><span class="sxs-lookup"><span data-stu-id="a5c43-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5c43-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="a5c43-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a5c43-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5c43-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a5c43-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a5c43-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="a5c43-111">傳回給應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5c43-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="a5c43-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="a5c43-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="a5c43-113">裝置類型的名稱或常數識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5c43-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="a5c43-114"> (裝置的名稱通常是從登錄或 SYSTEM.INI 檔案取得。 ) 如果這個成員是常數，它可以是 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a5c43-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5c43-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="a5c43-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="a5c43-116">裝置元素通常 (路徑) 。</span><span class="sxs-lookup"><span data-stu-id="a5c43-116">Device element (often a path).</span></span>

</dd> <dt>

<span data-ttu-id="a5c43-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="a5c43-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="a5c43-118">選用裝置別名。</span><span class="sxs-lookup"><span data-stu-id="a5c43-118">Optional device alias.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5c43-119">備註</span><span class="sxs-lookup"><span data-stu-id="a5c43-119">Remarks</span></span>

<span data-ttu-id="a5c43-120">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="a5c43-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c43-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5c43-121">Requirements</span></span>



| <span data-ttu-id="a5c43-122">需求</span><span class="sxs-lookup"><span data-stu-id="a5c43-122">Requirement</span></span> | <span data-ttu-id="a5c43-123">值</span><span class="sxs-lookup"><span data-stu-id="a5c43-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5c43-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c43-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5c43-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a5c43-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5c43-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c43-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5c43-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a5c43-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a5c43-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5c43-129"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5c43-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5c43-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5c43-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c43-131">**Mci**</span><span class="sxs-lookup"><span data-stu-id="a5c43-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a5c43-132">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="a5c43-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a5c43-133">**開啟的 MCI \_**</span><span class="sxs-lookup"><span data-stu-id="a5c43-133">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="a5c43-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5c43-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

