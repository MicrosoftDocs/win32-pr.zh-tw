---
description: WiaTransferParams 會在 Windows 映像取得 (WIA) 執行時間系統轉換成 IWiaTransferCallback：： TransferCallback 方法的資料傳輸期間傳送至應用程式。
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: 'WiaTransferParams 結構 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998242"
---
# <a name="wiatransferparams-structure"></a><span data-ttu-id="15f19-103">WiaTransferParams 結構</span><span class="sxs-lookup"><span data-stu-id="15f19-103">WiaTransferParams structure</span></span>

<span data-ttu-id="15f19-104">**WiaTransferParams** 會在 Windows 映像取得 (WIA) 執行時間系統轉換成 [**IWiaTransferCallback：： TransferCallback**](-wia-iwiatransfercallback-transfercallback.md)方法的資料傳輸期間傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="15f19-104">The **WiaTransferParams** is transmitted to an application during a data transfer by the Windows Image Acquisition (WIA) run-time system to the [**IWiaTransferCallback::TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f19-105">語法</span><span class="sxs-lookup"><span data-stu-id="15f19-105">Syntax</span></span>


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a><span data-ttu-id="15f19-106">成員</span><span class="sxs-lookup"><span data-stu-id="15f19-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15f19-107">**lMessage**</span><span class="sxs-lookup"><span data-stu-id="15f19-107">**lMessage**</span></span>
</dt> <dd>

<span data-ttu-id="15f19-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="15f19-108">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="15f19-109">表示資料傳輸的狀態。</span><span class="sxs-lookup"><span data-stu-id="15f19-109">Indicates the status of the data transfer.</span></span>

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span data-ttu-id="15f19-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA \_ 傳送 \_ 訊息 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="15f19-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA\_TRANSFER\_MSG\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span data-ttu-id="15f19-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA \_ 傳送 \_ \_ 資料流程結尾 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15f19-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_STREAM**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span data-ttu-id="15f19-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA \_ 傳送 \_ 訊息 \_ 結束 \_ \_ 傳送**</span><span class="sxs-lookup"><span data-stu-id="15f19-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_TRANSFER**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span data-ttu-id="15f19-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA \_ 傳送 \_ MSG \_ 裝置 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="15f19-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA\_TRANSFER\_MSG\_DEVICE\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span data-ttu-id="15f19-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA \_ 傳送 \_ MSG 的 \_ 新 \_ 頁面**</span><span class="sxs-lookup"><span data-stu-id="15f19-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA\_TRANSFER\_MSG\_NEW\_PAGE**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="15f19-115">**lPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="15f19-115">**lPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="15f19-116">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="15f19-116">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="15f19-117">表示資料傳輸的進度（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="15f19-117">Indicates the progress of the data transfer as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="15f19-118">**ulTransferredBytes**</span><span class="sxs-lookup"><span data-stu-id="15f19-118">**ulTransferredBytes**</span></span>
</dt> <dd>

<span data-ttu-id="15f19-119">類型： **ULONG64**</span><span class="sxs-lookup"><span data-stu-id="15f19-119">Type: **ULONG64**</span></span>

</dd> <dd>

<span data-ttu-id="15f19-120">指出傳送的資料量。</span><span class="sxs-lookup"><span data-stu-id="15f19-120">Indicates the amount of data transferred.</span></span>

</dd> <dt>

<span data-ttu-id="15f19-121">**hrErrorStatus**</span><span class="sxs-lookup"><span data-stu-id="15f19-121">**hrErrorStatus**</span></span>
</dt> <dd>

<span data-ttu-id="15f19-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="15f19-122">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="15f19-123">驅動程式所設定之裝置的狀態或錯誤狀態;例如，「準備」。</span><span class="sxs-lookup"><span data-stu-id="15f19-123">The status, or error state, of the device set by the driver; for example, "warming up".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15f19-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="15f19-124">Requirements</span></span>



| <span data-ttu-id="15f19-125">需求</span><span class="sxs-lookup"><span data-stu-id="15f19-125">Requirement</span></span> | <span data-ttu-id="15f19-126">值</span><span class="sxs-lookup"><span data-stu-id="15f19-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15f19-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15f19-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15f19-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15f19-128">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15f19-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15f19-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15f19-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15f19-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15f19-131">標頭</span><span class="sxs-lookup"><span data-stu-id="15f19-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="15f19-132"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="15f19-132"><dt>Wia.h</dt></span></span> </dl> |



 

 




