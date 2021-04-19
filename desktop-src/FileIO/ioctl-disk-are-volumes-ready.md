---
description: 等候指定磁片上的所有磁片區都可供使用。
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: 'IOCTL_DISK_ARE_VOLUMES_READY 控制程式代碼 (Ntdddisk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979357"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a>IOCTL \_ 磁片 \_ 是磁片區 \_ \_ 就緒控制程式代碼

等候指定磁片上的所有磁片區都可供使用。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

磁片的控制碼。

若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式。

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

作業的控制項程式碼。

您 **\_ \_ \_ \_ 可以使用 IOCTL 磁片** 來進行此作業。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

未搭配此作業使用。 設定為 **Null**。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。 設定為 0 (零) 。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

未搭配此作業使用。 設定為 **Null**。

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

未搭配此作業使用。 設定為 0 (零) 。

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

未搭配此作業使用。 設定為 **Null**。

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。

如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。 在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構。 否則，函式會以無法預期的方式失敗。

針對重迭的作業， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。 否則，在作業完成或發生錯誤之前，函數不會傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成，表示磁片上的所有磁片區都已備妥可供使用， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntdddisk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[磁片管理控制碼](disk-management-control-codes.md)
</dt> </dl>

 

