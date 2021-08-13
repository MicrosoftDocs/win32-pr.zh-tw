---
title: 'IVMVirtualPC SearchPaths 屬性 (VPCCOMInterfaces .h) '
description: 用來尋找與 Windows Virtual PC 相關聯之檔案的檔案系統路徑。
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- SearchPaths 屬性 Virtual PC
- SearchPaths 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，SearchPaths 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ef75bf0a696494b839f330063ca310927a0d796829d96575721f492b8b691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471248"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>IVMVirtualPC：： SearchPaths 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取並設定用來尋找與 Windows Virtual PC 相關聯之檔案的檔案系統路徑。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a>屬性值

指定包含每個專案之檔案系統路徑的 safearray。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                               | 意義                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                               |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null**。<br/>                                                                                                  |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>                                 | *SearchPaths* 參數無效，無法剖析為路徑的陣列。<br/>                                    |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt> </dl> | 系統找不到在 *searchPaths* 參數中指定的目錄。<br/>                                                |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑) </dt> <dt>0x80070003</dt> </dl> | 系統找不到 *searchPaths* 參數所指定的路徑。<br/>                                                     |
| <dl> <dt>HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效) </dt> <dt>0x8007007b</dt> </dl>    | *SearchPaths* 參數中指定的路徑包含不合法的字元。 不合法的字元是 " \* ？ <>/ \| "： "。<br/> |
| <dl> <dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤) </dt> <dt>0x800700a1</dt> </dl>    | 包含在 *searchPaths* 參數中的路徑會指定空的或相對路徑。 需要絕對路徑。<br/>          |
| <dl> <dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出) </dt> <dt>0x8007006f</dt> </dl> | *SearchPaths* 參數中指定的路徑太長。 路徑長度必須少於260個字元。<br/>     |
| <dl> <dt>VM \_E \_ PREF \_ \_ 找不到</dt> <dt>0xA0040300</dt> </dl>                       | 找不到喜好設定。<br/>                                                                                               |
| <dl> <dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt> </dl>     | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/>                                        |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

