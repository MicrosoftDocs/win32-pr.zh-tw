---
description: 使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的來源字串轉譯成 Unicode 字串。
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: 'RtlUTF8ToUnicodeN 函式 (Wdm) '
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187668"
---
# <a name="rtlutf8tounicoden-function"></a>RtlUTF8ToUnicodeN 函式

使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的來源字串轉譯成 Unicode 字串。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*UnicodeStringDestination* \[擴展\]
</dt> <dd>

呼叫端配置的緩衝區的指標，此緩衝區會接收翻譯的字串。

</dd> <dt>

*UnicodeStringMaxByteCount* \[在\]
</dt> <dd>

要在 *UnicodeStringDestination* 寫入的最大位元組數目。 如果這個值導致轉譯的字串被截斷， **RtlUTF8ToUnicodeN** 會傳回錯誤狀態。

</dd> <dt>

*UnicodeStringActualByteCount* \[out、optional\]
</dt> <dd>

呼叫端組態變數的指標，此變數會接收翻譯字串的長度（以位元組為單位）。 這個參數是選擇性的，而且可以是 **Null**。 如果字串被截斷，傳回的數位就會計算實際截斷的字串計數。

</dd> <dt>

*UTF8StringSource* \[在\]
</dt> <dd>

要轉譯之字串的指標。

</dd> <dt>

*UTF8StringByteCount* \[在\]
</dt> <dd>

*UTF8StringSource* 中字串的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

**RtlUTF8ToUnicodeN** 會傳回下列其中一個 NTSTATUS 值：



| 傳回碼                                                                                                  | Description                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**狀態 \_ 成功**</dt> </dl>               | 字串已轉換成 Unicode。<br/>                                                                 |
| <dl> <dt>**狀態 \_ 部分 \_ 未 \_ 對應**</dt> </dl>     | 遇到不正確輸入字元，並被取代。 此狀態會被視為成功狀態。<br/> |
| <dl> <dt>**狀態 \_ 不正確 \_ 參數**</dt> </dl>    | *UnicodeStringDestination* 和 *UnicodeStringActualByteCount* 的兩個指標都是 **Null**。<br/>       |
| <dl> <dt>**狀態 \_ 不正確 \_ 參數 \_ 4**</dt> </dl> | *UTF8StringSource* 為 **Null**。<br/>                                                                 |
| <dl> <dt>**狀態 \_ 緩衝區 \_ 太 \_ 小**</dt> </dl>    | *UnicodeStringDestination* 已被截斷。<br/>                                                            |



 

## <a name="remarks"></a>備註

雖然 *UnicodeStringActualByteCount* 是選擇性的，而且可以是 **Null**，但呼叫端應該提供它的儲存空間，因為接收的長度可以用來判斷轉換是否成功。

如果輸出已截斷並遇到不正確輸入字元，則函式會傳回狀態 \_ 緩衝區 \_ 太 \_ 小的錯誤。

如果 *UnicodeStringDestination* 設定為 **Null** ，則函式會傳回所需的位元組數目來裝載轉譯的字串，而不會在 *UnicodeStringActualByteCount* 中進行任何截斷。

除非 *UnicodeStringDestination* 和 *UTF8StringSource* 指標相等，否則 **RtlUTF8ToUnicodeN** 不會修改來源字串。 傳回的 Unicode 字串不是以 null 結束。

**RtlUTF8ToUnicodeN** 的呼叫端必須以 IRQL < 分派 \_ 層級執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wdm</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RtlUnicodeToUTF8N**](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




