---
description: Revert 方法會捨棄自從上次 IByteBuffer：： Commit 呼叫之後對交易資料流程所做的所有變更。
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'IByteBuffer：： Revert 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191274"
---
# <a name="ibytebufferrevert-method"></a>IByteBuffer：： Revert 方法

\[**Revert** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Revert** 方法會捨棄自從上次 [**IByteBuffer：： Commit**](ibytebuffer-commit.md)呼叫之後對交易資料流程所做的所有變更。

## <a name="syntax"></a>語法


```C++
HRESULT Revert();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 \_ [確定] 表示呼叫成功，而且資料流程已還原為先前的版本。

## <a name="remarks"></a>備註

這個方法會捨棄自上次認可作業之後對交易資料流程所做的變更。

## <a name="examples"></a>範例

下列範例會示範如何將交易資料流程還原至最後認可的作業。


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
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



 

