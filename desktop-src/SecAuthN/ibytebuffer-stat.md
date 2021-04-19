---
description: Stat 方法會從資料流程物件中捕獲統計資訊。
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'IByteBuffer：： Stat 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985323"
---
# <a name="ibytebufferstat-method"></a>IByteBuffer：： Stat 方法

\[**Stat** 方法可在 [需求] 區段中指定的作業系統中使用。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Stat** 方法會從資料流程物件中捕獲統計資訊。

## <a name="syntax"></a>語法


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pstatstg* \[擴展\]
</dt> <dd>

指向 **STATSTRUCT** 結構，這個方法會在其中放置此資料流程物件的相關資訊。 如果發生錯誤，此指標會是 **Null** 。

</dd> <dt>

*grfStatFlag* \[在\]
</dt> <dd>

指定此方法不會傳回 **STATSTRUCT** 結構中的某些欄位，因此會儲存記憶體配置作業。 值取自 [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) 列舉

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

**IByteBuffer：： Stat** 方法會抓取 **STATSTRUCT** 結構的指標，其中包含這個開啟資料流程的相關資訊。

## <a name="examples"></a>範例

下列範例會示範如何從資料流程中取出統計資訊。


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardssp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

