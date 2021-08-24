---
description: 使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的 Unicode 字串轉譯成新的字元字串。
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: 'RtlUnicodeToUTF8N 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3580eb86deba77bcc214cf69fbd21f65fee2735ef3a5ff73319b415d2c814d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538028"
---
# <a name="rtlunicodetoutf8n-function"></a>RtlUnicodeToUTF8N 函式

使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的 Unicode 字串轉譯成新的字元字串。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*UTF8StringDestination* \[擴展\]
</dt> <dd>

呼叫端配置的緩衝區指標，用來接收翻譯的字串。

</dd> <dt>

*UTF8StringMaxByteCount* \[在\]
</dt> <dd>

要寫入至 *UTF8StringDestination* 的最大位元組數目。 如果這個值導致轉譯的字串被截斷， **RtlUnicodeToUTF8N** 會傳回錯誤狀態。

</dd> <dt>

*UTF8StringActualByteCount* \[out、optional\]
</dt> <dd>

呼叫端組態變數的指標，此變數會接收翻譯字串的長度（以位元組為單位）。 這個參數是選擇性的，而且可以是 **Null**。 如果字串被截斷，傳回的數位就會計算實際截斷的字串計數。

</dd> <dt>

*UnicodeStringSource* \[在\]
</dt> <dd>

要轉譯的 Unicode 來源字串指標。

</dd> <dt>

* UnicodeStringByteCount * \[ in\]
</dt> <dd>

指定 *UnicodeStringSource* 參數指向的 Unicode 來源字串中的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

**RtlUnicodeToUTF8N** 會傳回下列其中一個 NTSTATUS 值：



| 傳回碼                                                                                                  | 描述                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**狀態 \_ 成功**</dt> </dl>               | Unicode 字串已轉換為 UTF-8。<br/>                                                           |
| <dl> <dt>**狀態 \_ 部分 \_ 未 \_ 對應**</dt> </dl>     | 遇到不正確輸入字元，並被取代。 此狀態會被視為成功狀態。<br/> |
| <dl> <dt>**狀態 \_ 不正確 \_ 參數**</dt> </dl>    | *UTF8StringDestination* 和 *UTF8StringActualByteCount* 的兩個指標都是 **Null**。<br/>              |
| <dl> <dt>**狀態 \_ 不正確 \_ 參數 \_ 4**</dt> </dl> | *UnicodeStringSource* 為 **Null**。<br/>                                                              |
| <dl> <dt>**狀態 \_ 緩衝區 \_ 太 \_ 小**</dt> </dl>    | *UTF8StringDestination* 已被截斷。<br/>                                                               |



 

## <a name="remarks"></a>備註

雖然 *UTF8StringActualByteCount* 是選擇性的，而且可以是 **Null**，但呼叫端應該提供它的儲存空間，因為接收的長度可以用來判斷轉換是否成功。 此常式不會修改來源字串。 如果指定的 *UnicodeStringSource* 包含 null 結束字元，且給定的 *UTF8StringMaxByteCount* 不會造成截斷，則會傳回以 null 終止的 utf-8 字串。

如果輸出已截斷並遇到不正確輸入字元，則函式會傳回狀態 \_ 緩衝區 \_ 太 \_ 小的錯誤。

如果 *UTF8StringDestination* 設定為 **Null** ，則函式會傳回所需的位元組數目來裝載轉譯的字串，而不會在 *UTF8StringActualByteCount* 中進行任何截斷。

**RtlUnicodeToUTF8N** 的呼叫端必須以 IRQL < 分派 \_ 層級執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wdm</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




