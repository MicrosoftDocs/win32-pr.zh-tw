---
description: 提供用來建立 class factory 的範本。
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: 'CFactoryTemplate 類別 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000866"
---
# <a name="cfactorytemplate-class"></a>CFactoryTemplate 類別

提供用來建立 class factory 的範本。

在 DirectShow 中，會使用 **CFactoryTemplate** 類別（也稱為 *factory 範本*）來特製化類別 factory。 每個 class factory 都會保留一個指向 factory 範本的指標。 Factory 範本包含 COM 物件的相關資訊，包括物件的類別識別碼 (CLSID) 和函式的指標，該函式會建立物件。

在您的 DLL 中，宣告名為 *g \_ templates* 的原廠範本的全域陣列。 針對 DLL 中的每個物件，各包含一個 factory 範本。 當 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式建立新的 class factory 時，它會在陣列中搜尋具有相符 CLSID 的範本。 假設找到一個，它會建立一個持有相符範本指標的 class factory。 當用戶端呼叫 **IClassFactory：： CreateInstance** 時，class factory 會呼叫範本中定義的具現化函數。

如需詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。



| Public 成員變數                                                   | Description                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ 名稱**](cfactorytemplate-m-name.md)                                | 篩選的名稱。                                                        |
| [**m \_ ClsID**](cfactorytemplate-m-clsid.md)                              | 物件之 CLSID 的指標。                                        |
| [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md)                          | 函數的指標，該函式會建立物件的實例。              |
| [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)                        | 從 DLL 進入點呼叫之函式的指標。           |
| [**m \_ pAMovieSetup \_ 篩選**](cfactorytemplate-m-pamoviesetup-filter.md) | [**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md)結構的指標。 |
| 公用方法                                                            | Description                                                                |
| [**IsClassID**](cfactorytemplate-isclassid.md)                           | 判斷 CLSID 是否符合這個類別範本。                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | 呼叫類別的物件建立函數。                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>Strmbase .lib;</dt><dt>Strmbasd .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[基類參考](base-class-reference.md)
</dt> </dl>

 

