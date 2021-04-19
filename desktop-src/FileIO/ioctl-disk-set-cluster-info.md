---
description: 設定磁片上的叢集資訊。
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: 'IOCTL_DISK_SET_CLUSTER_INFO 控制程式代碼 (Ntdddisk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988990"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a>IOCTL \_ 磁片 \_ 設定 \_ 叢集 \_ 資訊控制程式代碼

設定磁片上的叢集資訊。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
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

請使用 **IOCTL \_ 磁片集叢集 \_ \_ \_ 資訊** 進行這種操作。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

[**磁片 \_ 群集 \_ 資訊**](disk-cluster-info.md)資料結構的指標，其中包含磁片的叢集資訊。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

未搭配此作業使用。 設定為 **Null**。

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。 設定為 0 (零) 。

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
| 最低支援的用戶端<br/> | 都不支援<br/>                                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntdddisk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[磁片管理控制碼](disk-management-control-codes.md)
</dt> <dt>

[**磁片 \_ 群集 \_ 資訊**](disk-cluster-info.md)
</dt> <dt>

[**IOCTL \_ 磁片 \_ 取得 \_ 叢集 \_ 資訊**](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

