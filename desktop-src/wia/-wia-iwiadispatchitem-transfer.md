---
description: Item 物件的 Transfer 方法會將資料從裝置傳送到檔案。 此方法僅適用于裝置類型專案。
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986385"
---
# <a name="itemtransfer-method"></a><span data-ttu-id="78538-104">Item. Transfer 方法</span><span class="sxs-lookup"><span data-stu-id="78538-104">Item.Transfer method</span></span>

<span data-ttu-id="78538-105">[**Item**](-wia-item.md)物件的 **Transfer** 方法會將資料從裝置傳送到檔案。</span><span class="sxs-lookup"><span data-stu-id="78538-105">The **Transfer** method of the [**Item**](-wia-item.md) object transfers data from a device to a file.</span></span> <span data-ttu-id="78538-106">此方法僅適用于裝置類型專案。</span><span class="sxs-lookup"><span data-stu-id="78538-106">This method applies only to device type items.</span></span>

## <a name="syntax"></a><span data-ttu-id="78538-107">語法</span><span class="sxs-lookup"><span data-stu-id="78538-107">Syntax</span></span>


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a><span data-ttu-id="78538-108">參數</span><span class="sxs-lookup"><span data-stu-id="78538-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78538-109">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78538-109">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78538-110">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="78538-110">Type: **BSTR**</span></span>

<span data-ttu-id="78538-111">指定要將資料傳輸至其中的檔案名。</span><span class="sxs-lookup"><span data-stu-id="78538-111">Specifies the name of the file to which the data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="78538-112">*AsyncTransfer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78538-112">*AsyncTransfer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78538-113">Type： **VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="78538-113">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="78538-114">布林值，指定是否應該以非同步呼叫來執行傳送。</span><span class="sxs-lookup"><span data-stu-id="78538-114">A Boolean value that specifies whether the transfer should be run as an asynchronous call.</span></span>

<dt>



 <span data-ttu-id="78538-115"> (VARIANT \_ BOOL) </span><span class="sxs-lookup"><span data-stu-id="78538-115">(VARIANT\_BOOL)</span></span>


</dt> <dd>

<span data-ttu-id="78538-116">預設值。</span><span class="sxs-lookup"><span data-stu-id="78538-116">Default.</span></span> <span data-ttu-id="78538-117">如果呼叫應該是非同步，請將此值設定為 **true** ， (查看 **備註**) 。</span><span class="sxs-lookup"><span data-stu-id="78538-117">Set this value to **true** if the call should be asynchronous (see **Remarks**).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78538-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="78538-118">Return value</span></span>

<span data-ttu-id="78538-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="78538-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78538-120">備註</span><span class="sxs-lookup"><span data-stu-id="78538-120">Remarks</span></span>

<span data-ttu-id="78538-121">這個方法只適用于檔案類型專案。</span><span class="sxs-lookup"><span data-stu-id="78538-121">This method applies only to file type items.</span></span> <span data-ttu-id="78538-122">方法會先檢查項目是否支援這個方法，然後再嘗試完成資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="78538-122">The method checks that the item supports this method before it attempts to complete the data transfer.</span></span>

<span data-ttu-id="78538-123">使用 "剪貼簿" 作為 *Filename* 參數，將專案傳送至剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="78538-123">Use "clipboard" as the *Filename* parameter to transfer an item to the clipboard.</span></span>

<span data-ttu-id="78538-124">將 *AsyncTransfer* 值設定為 **false** ，以在任何在腳本結束時終止進程的環境中執行的應用程式或腳本內進行傳輸，例如 WINDOWS script Host (WSH) 。</span><span class="sxs-lookup"><span data-stu-id="78538-124">Set the *AsyncTransfer* value to **false** for transfers within any application or script that runs in an environment that terminates a process at the end of a script, such as Windows Script Host (WSH).</span></span> <span data-ttu-id="78538-125">否則，腳本可能會結束，且進程會在傳送完成之前終止。</span><span class="sxs-lookup"><span data-stu-id="78538-125">Otherwise, the script may end, and the process terminate, before the transfer completes.</span></span>

<span data-ttu-id="78538-126">傳送方法沒有 **傳回** 值。</span><span class="sxs-lookup"><span data-stu-id="78538-126">The **Transfer** method has no return value.</span></span> <span data-ttu-id="78538-127">完成傳送時，此方法會將 [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) 事件傳送至腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="78538-127">Upon completion of a transfer, this method sends an [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) event to the script or application.</span></span>

## <a name="examples"></a><span data-ttu-id="78538-128">範例</span><span class="sxs-lookup"><span data-stu-id="78538-128">Examples</span></span>

<span data-ttu-id="78538-129">下列範例示範如何使用 **傳送** 方法，從裝置傳送資料。</span><span class="sxs-lookup"><span data-stu-id="78538-129">The following example demonstrates the use of the **Transfer** method to transfer data from a device.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="78538-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="78538-130">Requirements</span></span>



| <span data-ttu-id="78538-131">需求</span><span class="sxs-lookup"><span data-stu-id="78538-131">Requirement</span></span> | <span data-ttu-id="78538-132">值</span><span class="sxs-lookup"><span data-stu-id="78538-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78538-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78538-133">Minimum supported client</span></span><br/> | <span data-ttu-id="78538-134">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78538-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78538-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78538-135">Minimum supported server</span></span><br/> | <span data-ttu-id="78538-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78538-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="78538-137">DLL</span><span class="sxs-lookup"><span data-stu-id="78538-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78538-138"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="78538-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




