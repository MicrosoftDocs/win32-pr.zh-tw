---
title: 'IVMVirtualPC DefaultVMConfigurationPath 屬性 (VPCCOMInterfaces .h) '
description: 要搜尋可用虛擬機器組態檔案的預設目錄。
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- DefaultVMConfigurationPath 屬性 Virtual PC
- DefaultVMConfigurationPath 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，DefaultVMConfigurationPath 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686215"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>IVMVirtualPC：:D efaultVMConfigurationPath 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取並設定要搜尋可用虛擬機器組態檔案的預設目錄。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a>屬性值

指定預設虛擬機器組態檔的目錄路徑。 在路徑字串中，反斜線 (\) 可能會緊接在結尾的 null 字元之前出現。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                               | 意義                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                                                 |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                    | *ConfigurationPath* 參數為 **Null**。<br/>                                                                                                |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt> </dl> | 系統找不到 *configurationPath* 參數所指定的目錄。<br/>                                                          |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑) </dt> <dt>0x80070003</dt> </dl> | 系統找不到 *configurationPath* 參數所指定的路徑。<br/>                                                               |
| <dl> <dt>HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效) </dt> <dt>0x8007007b</dt> </dl>    | *ConfigurationPath* 參數包含不正確字元 (下列其中一項： " \* ？ <>/ \| "： ") 。<br/>                                   |
| <dl> <dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤) </dt> <dt>0x800700a1</dt> </dl>    | *ConfigurationPath* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                                          |
| <dl> <dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出) </dt> <dt>0x8007006f</dt> </dl> | *ConfigurationPath* 參數所指定的路徑太長。 路徑的長度必須小於 **最大 \_ 路徑** (260) 個字元。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                                             |
| <dl> <dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt> </dl>     | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/>                                                          |



## <a name="remarks"></a>備註

根據預設，這個屬性值會設定為下列目錄： "% LocalAppData% \\ Microsoft \\ WINDOWS Virtual PC \\ 虛擬機器 \\ "。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

