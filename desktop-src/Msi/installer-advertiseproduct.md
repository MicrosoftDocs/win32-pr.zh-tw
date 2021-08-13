---
description: 安裝程式物件的 AdvertiseProduct 方法會通告安裝套件。
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: Installer：： AdvertiseProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a3792b279df9ac43fc09eaa02005cdaf3373e341bf2df40ce0a350d6c31bd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633287"
---
# <a name="installeradvertiseproduct-method"></a>Installer：： AdvertiseProduct 方法

[**安裝程式**](installer-object.md)物件的 **AdvertiseProduct** 方法會通告安裝套件。

## <a name="syntax"></a>語法


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*packagePath* 
</dt> <dd>

要公告的 Windows Installer 封裝 (.msi) 的完整路徑。

</dd> <dt>

*內容* 
</dt> <dd>

公告的內容。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt> </dl> | 在每一部電腦的 [安裝內容](installation-context.md)中，為安裝通告應用程式。 這讓封裝可供電腦的所有使用者進行安裝。<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**msiAdvertiseProductUser**</dt> <dt>1</dt> </dl>             | 在每個使用者 [安裝內容](installation-context.md)中通告應用程式以進行安裝。<br/>                                                                                   |



 

</dd> <dt>

*變換* 
</dt> <dd>

要套用至產品的轉換清單。 清單中的轉換會以分號分隔。 這是選擇性參數。

</dd> <dt>

*language* 
</dt> <dd>

要使用之安裝套件的語言。 這是選擇性參數。

</dd> <dt>

*options* 
</dt> <dd>

公告選項。 這是選擇性參數。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | 標準公告<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | 通告產品的新實例。 需要 *轉換* 參數之轉換清單中的第一個轉換是變更產品代碼的實例轉換。 如需詳細資訊，請參閱 [安裝多個產品和修補程式實例](installing-multiple-instances-of-products-and-patches.md)。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**AdvertiseProduct** 方法會使用 [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)函數。

## <a name="examples"></a>範例

下列範例示範如何使用 **AdvertiseProduct** 方法。


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 和 Windows XP 上的安裝程式4。5<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**安裝程式**](installer-object.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




