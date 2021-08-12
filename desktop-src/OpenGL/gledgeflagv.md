---
title: 'glEdgeFlagv 函式 (Gl) '
description: '將邊緣旗標為界限或 nonboundary。 |glEdgeFlagv 函式 (Gl) '
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- glEdgeFlagv 函式 OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9622cb3c7d80d241d0f12957094a06980f5fcf7f28b4f95eaa0de1595b34d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616530"
---
# <a name="gledgeflagv-function"></a>glEdgeFlagv 函式

將邊緣旗標為界限或 nonboundary。

## <a name="syntax"></a>語法


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* 
</dt> <dd>

指定陣列的指標，該陣列包含單一布林值元素，其會取代目前的邊緣旗標值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

多邊形、個別三角形或 [**glBegin**](/windows/desktop/OpenGL/glbegin)glEnd 配對之間指定之個別四邊形的每個頂點 / [](/windows/desktop/OpenGL/glend)都會標示為界限或 nonboundary 邊緣的起點。 當指定頂點時，如果目前的邊緣旗標為 **TRUE** ，則會將頂點標示為界限邊緣的起點。 如果目前的邊緣旗標為 **FALSE**，則會將頂點標示為 nonboundary 邊緣的開頭。 如果旗標為非零，則 **glEdgeFlagv** 函式會將邊緣旗標設定為 **TRUE** ，否則為 **FALSE** 。

無論邊緣旗標的值為何，連接的三角形和連接 quadrilaterals 的頂點一律會標示為界限。

只有當 GL \_ 多邊形 \_ 模式設定為 gl \_ 點或 gl 線時，頂點上的界限和 nonboundary 邊緣旗標才有意義 \_ 。 請參閱 [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode)。

一開始，邊緣旗標位為 **TRUE**。

您可以隨時更新目前的 edge 旗標。 尤其是，在呼叫 [**glBegin**](/windows/desktop/OpenGL/glbegin)和對應的 [**glEnd**](/windows/desktop/OpenGL/glend)呼叫之間，可以呼叫 **glEdgeFlagv** 。

下列函式會取出與 **glEdgeFlagv** 相關的資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 邊緣 \_ 旗標

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

