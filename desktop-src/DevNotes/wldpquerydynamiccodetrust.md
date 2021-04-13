---
description: 抓取值，這個值會判斷指定的記憶體中或磁片上的 .NET CRL 動態程式碼是否受到 Device Guard 原則的信任。
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: 'WldpQueryDynamicCodeTrust 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510528"
---
# <a name="wldpquerydynamiccodetrust-function"></a>WldpQueryDynamicCodeTrust 函式

抓取值，這個值會判斷指定的記憶體中或磁片上的 .NET CRL 動態程式碼是否受到 Device Guard 原則的信任。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fileHandle* 
</dt> <dd>

要檢查的磁片上動態程式碼檔案的控制碼。 如果 *fileHandle* 為非 **null**，則 *baseImage* 應該是 **null**。

</dd> <dt>

*baseImage* 
</dt> <dd>

要檢查之記憶體中 PE 檔案的指標。 如果 *baseImage* 為非 **null**，則 *FileHandle* 應該是 **null**。

</dd> <dt>

*ImageSize* 
</dt> <dd>

當 *baseImage* 為非 **Null** 時，表示 *baseImage* 所指向的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




