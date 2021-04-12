---
title: 'VMFloppyDiskImageType 列舉 (VPCCOMInterfaces) '
description: 指定磁片格式。
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- VMFloppyDiskImageType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384629"
---
# <a name="vmfloppydiskimagetype-enumeration"></a>VMFloppyDiskImageType 列舉

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定磁片格式。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage \_ 不明**
</dt> <dd>

未知的格式。

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage \_ LowDensity**
</dt> <dd>

低密度格式 (720K) 。

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage \_ HighDensity**
</dt> <dd>

高密度格式 (1.44 MB) 。

</dd> <dt>

<span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage \_ DMF**
</dt> <dd>

 (1.68 Mb) 的散發媒體格式。

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage \_ LowDensitySingleSided**
</dt> <dd>

單面低密度格式。

</dd> <dt>

<span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage \_ MediumDensity**
</dt> <dd>

 (1.2 MB) 的中等密度格式。

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage \_ HighDensityMSS**
</dt> <dd>

高密度的多重磁區大小 (MSS) ， (XDF) 的延伸發佈格式使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC::CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[**IVMVirtualPC::GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

