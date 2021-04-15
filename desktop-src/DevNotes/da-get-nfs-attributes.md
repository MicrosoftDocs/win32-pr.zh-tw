---
description: DA \_ GET \_ nfs \_ 屬性控制程式代碼會查詢其他有關 NFS 共用的資訊。
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES 控制程式代碼
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510504"
---
# <a name="da_get_nfs_attributes-control-code"></a>DA \_ GET \_ NFS \_ 屬性控制項程式碼

**DA \_ GET \_ nfs \_ 屬性** 控制程式代碼會查詢其他有關 NFS 共用的資訊。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* \[在\]
</dt> <dd>

NFS 共用上檔案的控制碼。 若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。

</dd> <dt>

*dwIoControlCode* \[在\]
</dt> <dd>

作業的控制項程式碼。 請使用 **DA \_ GET \_ NFS \_ 屬性** 進行這種操作。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

未搭配此作業使用;設定為 **Null**。

</dd> <dt>

*nInBufferSize* \[在\]
</dt> <dd>

未搭配此作業使用;設定為零。

</dd> <dt>

*lpOutBuffer* \[擴展\]
</dt> <dd>

輸出緩衝區的指標，其中包含 **NFS \_ 檔 \_ 屬性** 結構。 如需詳細資訊，請參閱＜備註＞一節。

</dd> <dt>

*nOutBufferSize* \[在\]
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。

</dd> <dt>

*lpBytesReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。

如果輸出緩衝區太小，則呼叫會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **錯誤的 \_ \_ 緩衝區**，而 *lpBytesReturned* 為零。

如果 *lpOverlapped* 為 **null**，則 *lpBytesReturned* 不可以是 **null**。 即使作業未傳回輸出資料，而且 *lpOutBuffer* 為 **Null**， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 也會使用 *lpBytesReturned*。 在這類作業之後， *lpBytesReturned* 的值就沒有意義。

如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。 如果這個參數不是 **Null** ，而且作業傳回資料，則 *lpBytesReturned* 會在重迭的作業完成之前無意義。 若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)。 如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* \[在\]
</dt> <dd>

重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。

如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。 在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭結構。 否則，函式會以無法預期的方式失敗。

針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。 否則，在作業完成或發生錯誤之前，函數不會傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

此控制項程式碼沒有相關聯的標頭檔。 您必須定義控制項程式碼和資料結構，如下所示。

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

結構成員可以如下描述。

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

用於特殊檔案類型的不透明值，例如區塊特殊、字元特殊和 FIFO 檔案。

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

用於特殊檔案類型的不透明值，例如區塊特殊、字元特殊和 FIFO 檔案。

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**秒**
</dt> <dd>

表示自1970年1月1日起的秒數 (UTC) 的64位值。

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

要加入至 **秒** 成員的毫微秒數。

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**
</dt> <dd>

共用的 NFS 檔案類型。



| NFS 檔案類型                                                                              | Description                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS \_ 類型 \_ REG<br/>    | 一般檔案。<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS \_ 類型 \_ 目錄<br/>    | 目錄。<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS \_ 類型 \_ BLK<br/>    | 區塊-特殊檔案。<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS \_ 類型 \_ CHR<br/>    | 字元-特殊檔案。<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS \_ 類型 \_ .LNK<br/>    | 符號連結。<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS \_ 類型 \_ SOCK<br/> | Windows 通訊端。<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS \_ 類型 \_ FIFO<br/> | FIFO 檔。<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**模式**
</dt> <dd>

檔案模式。

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

共用的連結數目。

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**
</dt> <dd>

UNIX 使用者識別碼 (UID) 。

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**
</dt> <dd>

UNIX 群組識別碼 (GID) 。

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**大小**
</dt> <dd>

檔案大小（以位元組為單位）。

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**使用**
</dt> <dd>

使用的檔案大小（以位元組為單位）。 這與檔案大小相同。

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

裝置識別碼。

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

檔案系統識別碼。

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**
</dt> <dd>

檔案識別碼。

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**
</dt> <dd>

上次存取時間。

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**
</dt> <dd>

上次修改時間。

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

上次變更時間。

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**
</dt> <dd>

**NFS \_ 檔 \_ 屬性** 結構。

> [!Note]  
> 如需此結構成員的詳細說明，請參閱「NFS 版本3通訊協定規格」中的 **fattr3** 結構 (，如 [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)) 中所定義。

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**版本**
</dt> <dd>

指定是否透過 NFS 版本2或 NFS 第3版通訊協定來建立 NFS 共用的控制碼連線。



| 值                            | 描述              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | NFS 版本2<br/> |
| <span id="3"></span>3<br/> | NFS 版本3<br/> |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>    |
| 用戶端支援結束<br/>    | 都不支援<br/>         |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
