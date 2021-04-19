---
title: IConfigAsfWriter2 GetParam 方法
description: GetParam 方法會抓取指定之篩選準則設定參數的目前值。
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- GetParam 方法 windows Media 格式
- GetParam 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，GetParam 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966471"
---
# <a name="iconfigasfwriter2getparam-method"></a>IConfigAsfWriter2：： GetParam 方法

**GetParam** 方法會抓取指定之篩選準則設定參數的目前值。

## <a name="syntax"></a>語法


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwParam* \[在\]
</dt> <dd>

指定要取出的參數。 它必須是[ \_ AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))列舉中所定義的值。

</dd> <dt>

*pdwParam1* \[擴展\]
</dt> <dd>

變數的指標，該變數會抓取 *dwParam* 中指定之參數的值。

</dd> <dt>

*pdwParam2* \[擴展\]
</dt> <dd>

未使用，必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2：： SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 