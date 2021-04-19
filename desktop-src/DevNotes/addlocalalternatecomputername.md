---
description: 為呼叫它的電腦新增替代局域網路名稱。
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987889"
---
# <a name="addlocalalternatecomputername-function"></a>AddLocalAlternateComputerName 函式

為呼叫它的電腦新增替代局域網路名稱。

## <a name="syntax"></a>語法


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpDnsFQHostname* \[在\]
</dt> <dd>

要加入的替代名稱。 名稱必須是 **ComputerNameDnsFullyQualified** 格式，如 [**電腦 \_ 名稱 \_ 格式**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) 列舉中所定義，而且 [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) 函數必須能夠驗證它的格式設定為 **DnsNameHostnameFull**。

</dd> <dt>

*ulFlags* \[在\]
</dt> <dd>

此參數是保留的，而且必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 **錯誤 \_ SUCCESS**。 如果函式失敗，則會傳回非零的錯誤碼。 它傳回的錯誤碼如下：



| 傳回碼                                                                                               | Description                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>  | 指出 *lpDnsFQHostname* 參數未指向有效的 DNS 名稱，或 *ulFlags* 參數不等於零。<br/> |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl> | 記憶體不足，無法完成此作業。<br/>                                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| 程式庫<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Unicode 與 ANSI 名稱<br/> | **AddLocalAlternateComputerNameW** (Unicode) 和 **AddLocalAlternateComputerNameA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電腦 \_ 名稱 \_ 格式**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
