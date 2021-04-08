---
description: ID3DX10ThreadPump 介面使用的資料處理物件，以非同步方式處理載入的資料。
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: 'ID3DX10DataProcessor 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854096"
---
# <a name="id3dx10dataprocessor-interface"></a>ID3DX10DataProcessor 介面

[**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)使用的資料處理物件，以非同步方式處理載入的資料。

## <a name="members"></a>成員

**ID3DX10DataProcessor** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10DataProcessor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10DataProcessor** 介面具有這些方法。



| 方法                                                                | 描述                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | 建立裝置物件。<br/>                                                                                                  |
| [**摧毀**](id3dx10dataprocessor-destroy.md)                       | 在工作專案完成後， [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md) 用來終結處理器。<br/> |
| [**處理序**](id3dx10dataprocessor-process.md)                       | 處理一些資料。<br/>                                                                                                       |



 

## <a name="remarks"></a>備註

可以繼承這個物件，並重新定義其成員。 這麼做可讓您自訂 API 來處理您自己的自訂檔案格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
