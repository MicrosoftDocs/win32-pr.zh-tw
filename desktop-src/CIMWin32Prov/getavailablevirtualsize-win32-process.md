---
description: 抓取進程可用之可用虛擬位址空間的目前大小（以位元組為單位）。
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Win32_Process 類別的 GetAvailableVirtualSize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971952"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Win32 進程類別的 GetAvailableVirtualSize 方法 \_

抓取進程可用之可用虛擬位址空間的目前大小（以位元組為單位）。

## <a name="syntax"></a>語法


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AvailableVirtualSize* \[擴展\]
</dt> <dd>

*AvailableVirtualSize* 參數會傳回此進程可用的可用虛擬位址空間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成**
</dt> <dd>

0

作業已成功完成。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

使用者無法存取所要求的資訊

</dd> <dt>

**許可權不足**
</dt> <dd>

3

使用者沒有足夠的許可權。

</dd> <dt>

**未知的失敗**
</dt> <dd>

8

未知的失敗。

</dd> <dt>

**找不到路徑**
</dt> <dd>

9

指定的路徑不存在。

</dd> <dt>

**參數不正確**
</dt> <dd>

21

指定的參數無效。

</dd> <dt>

**其他**
</dt> <dd>

22 4294967295

針對列出的值以外的值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 檔。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 進程**](win32-process.md)
</dt> </dl>

 

