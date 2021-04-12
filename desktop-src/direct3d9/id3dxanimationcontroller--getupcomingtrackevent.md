---
description: 傳回在動畫播放軌上指定的事件之後，排定要發生之下一個事件的事件控制碼。
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'ID3DXAnimationController：： GetUpcomingTrackEvent 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946054"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>ID3DXAnimationController：： GetUpcomingTrackEvent 方法

傳回在動畫播放軌上指定的事件之後，排定要發生之下一個事件的事件控制碼。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

追蹤識別碼。

</dd> <dt>

*hEvent* \[在\]
</dt> <dd>

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

指定事件的事件控制碼，之後會在此搜尋下列事件。 如果設定為 **Null**，則方法會傳回下一個排程的事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

排定在指定的追蹤上執行的下一個事件的事件控制碼。如果未排定任何新的事件，則會傳回 **Null** 。

## <a name="remarks"></a>備註

您可以重複將 **Null** 傳遞給 hEvent，以反復地使用這個方法來尋找所需的事件。

> [!Note]  
> 當方法傳回 **Null** 之後，請勿再逐一查看。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
