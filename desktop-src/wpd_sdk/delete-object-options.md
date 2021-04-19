---
description: 刪除 \_ 物件 \_ 選項列舉型別描述刪除物件時，裝置所支援的選項。
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: 'DELETE_OBJECT_OPTIONS 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999259"
---
# <a name="delete_object_options-enumeration"></a><span data-ttu-id="7fe0f-103">刪除 \_ 物件 \_ 選項列舉</span><span class="sxs-lookup"><span data-stu-id="7fe0f-103">DELETE\_OBJECT\_OPTIONS enumeration</span></span>

<span data-ttu-id="7fe0f-104">**刪除 \_ 物件 \_ 選項** 列舉型別描述刪除物件時，裝置所支援的選項。</span><span class="sxs-lookup"><span data-stu-id="7fe0f-104">The **DELETE\_OBJECT\_OPTIONS** enumeration type describes options that are supported by a device when deleting an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fe0f-105">Syntax</span></span>


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="7fe0f-106">常數</span><span class="sxs-lookup"><span data-stu-id="7fe0f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7fe0f-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**便攜 \_ 設備 \_ 刪除 \_ 沒有 \_ 遞迴**</span><span class="sxs-lookup"><span data-stu-id="7fe0f-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_NO\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="7fe0f-108">只刪除物件，如果它有子系，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="7fe0f-108">Delete the object only and fail if it has children.</span></span>

</dd> <dt>

<span data-ttu-id="7fe0f-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ \_ 使用遞迴的可攜式裝置刪除 \_**</span><span class="sxs-lookup"><span data-stu-id="7fe0f-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_WITH\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="7fe0f-110">刪除物件及其所有子系。</span><span class="sxs-lookup"><span data-stu-id="7fe0f-110">Delete the object and all its children.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fe0f-111">備註</span><span class="sxs-lookup"><span data-stu-id="7fe0f-111">Remarks</span></span>

<span data-ttu-id="7fe0f-112">應用程式可以藉由呼叫 [**IPortableDeviceCapabilities：： GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) 來取得裝置支援的刪除選項，以執行 **WPD \_ 命令物件管理的 [ \_ \_ \_ 刪除 \_ 物件** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="7fe0f-112">The application can retrieve the deletion options that the device supports by calling [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) for the **WPD\_COMMAND\_OBJECT\_MANAGEMENT\_DELETE\_OBJECTS** command.</span></span> <span data-ttu-id="7fe0f-113">它應該會檢查此方法在 [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)物件中傳回的 **WPD \_ 選項 \_ 物件 \_ 管理 \_ 遞迴 \_ 刪除 \_ 支援** 的選項值。</span><span class="sxs-lookup"><span data-stu-id="7fe0f-113">It should examine the **WPD\_OPTION\_OBJECT\_MANAGEMENT\_RECURSIVE\_DELETE\_SUPPORTED** option value that this method returns in an [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe0f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fe0f-114">Requirements</span></span>



| <span data-ttu-id="7fe0f-115">需求</span><span class="sxs-lookup"><span data-stu-id="7fe0f-115">Requirement</span></span> | <span data-ttu-id="7fe0f-116">值</span><span class="sxs-lookup"><span data-stu-id="7fe0f-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe0f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7fe0f-117">Header</span></span><br/> | <dl> <span data-ttu-id="7fe0f-118"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe0f-118"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe0f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fe0f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe0f-120">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="7fe0f-120">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




