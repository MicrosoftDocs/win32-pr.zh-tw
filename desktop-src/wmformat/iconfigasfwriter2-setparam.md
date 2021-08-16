---
title: IConfigAsfWriter2 SetParam 方法
description: SetParam 方法會設定指定之篩選設定參數的值。
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- SetParam 方法 windows Media 格式
- SetParam 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，SetParam 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e7c73831ec45e6e0b65444e93e976fe349a2d4576d578f3399c60c399628cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847496"
---
# <a name="iconfigasfwriter2setparam-method"></a>IConfigAsfWriter2：： SetParam 方法

**SetParam** 方法會設定指定之篩選設定參數的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwParam* \[在\]
</dt> <dd>

指定要設定的參數。 它必須是[ \_ AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))列舉中所定義的值。

</dd> <dt>

*dwParam1* \[在\]
</dt> <dd>

指定要指派給 *dwParam* 參數的值。

</dd> <dt>

*dwParam2* \[在\]
</dt> <dd>

未使用;必須是0。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2：： GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 