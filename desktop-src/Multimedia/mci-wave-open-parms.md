---
title: 'MCI_WAVE_OPEN_PARMS 結構 (Mciapi .h) '
description: MCI \_ WAVE \_ open PARMS 結構包含適用于 wave \_ 音訊裝置的 mci \_ open 命令資訊。
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- MCI_WAVE_OPEN_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966517"
---
# <a name="mci_wave_open_parms-structure"></a><span data-ttu-id="37524-104">MCI \_ WAVE \_ 開啟 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="37524-104">MCI\_WAVE\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="37524-105">**Mci \_ WAVE \_ open \_ PARMS** 結構包含適用于 wave 音訊裝置的 [**mci \_ open**](mci-open.md)命令資訊。</span><span class="sxs-lookup"><span data-stu-id="37524-105">The **MCI\_WAVE\_OPEN\_PARMS** structure contains information for [**MCI\_OPEN**](mci-open.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="37524-106">語法</span><span class="sxs-lookup"><span data-stu-id="37524-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="37524-107">成員</span><span class="sxs-lookup"><span data-stu-id="37524-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="37524-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="37524-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="37524-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="37524-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="37524-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="37524-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="37524-111">識別碼傳回至應用程式。</span><span class="sxs-lookup"><span data-stu-id="37524-111">Indentifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="37524-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="37524-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="37524-113">裝置類型的名稱或常數識別碼。</span><span class="sxs-lookup"><span data-stu-id="37524-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="37524-114"> (裝置的名稱通常是從登錄或 SYSTEM.INI 檔案取得。 ) 此成員可以是 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="37524-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="37524-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="37524-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="37524-116">裝置元素名稱通常 (路徑) 。</span><span class="sxs-lookup"><span data-stu-id="37524-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="37524-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="37524-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="37524-118">選用裝置別名。</span><span class="sxs-lookup"><span data-stu-id="37524-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="37524-119">**dwBufferSeconds**</span><span class="sxs-lookup"><span data-stu-id="37524-119">**dwBufferSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="37524-120">緩衝區長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="37524-120">Buffer length, in seconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37524-121">備註</span><span class="sxs-lookup"><span data-stu-id="37524-121">Remarks</span></span>

<span data-ttu-id="37524-122">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="37524-122">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="37524-123">如果您不是使用擴充的資料成員，您可以使用 [**mci \_ open \_ PARMS**](mci-open-parms.md) 結構，而不是 **mci \_ WAVE \_ open \_ PARMS** 。</span><span class="sxs-lookup"><span data-stu-id="37524-123">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure instead of **MCI\_WAVE\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="37524-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="37524-124">Requirements</span></span>



| <span data-ttu-id="37524-125">需求</span><span class="sxs-lookup"><span data-stu-id="37524-125">Requirement</span></span> | <span data-ttu-id="37524-126">值</span><span class="sxs-lookup"><span data-stu-id="37524-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37524-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37524-127">Minimum supported client</span></span><br/> | <span data-ttu-id="37524-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37524-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="37524-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37524-129">Minimum supported server</span></span><br/> | <span data-ttu-id="37524-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37524-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="37524-131">標頭</span><span class="sxs-lookup"><span data-stu-id="37524-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="37524-132"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="37524-132"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37524-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37524-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37524-134">**Mci**</span><span class="sxs-lookup"><span data-stu-id="37524-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="37524-135">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="37524-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="37524-136">**開啟的 MCI \_**</span><span class="sxs-lookup"><span data-stu-id="37524-136">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="37524-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37524-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="37524-138">**MCI \_ 開啟 \_ PARMS**</span><span class="sxs-lookup"><span data-stu-id="37524-138">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> </dl>

 

