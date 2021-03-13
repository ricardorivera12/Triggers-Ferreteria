# Triggers-Ferreteria
<jasperReport xmlns="http://jasperreports.sourceforge.net/jasperreports" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports http://jasperreports.sourceforge.net/xsd/jasperreport.xsd" name="river2" language="groovy" pageWidth="842" pageHeight="595" orientation="Landscape" columnWidth="802" leftMargin="20" rightMargin="20" topMargin="20" bottomMargin="20" uuid="82480de7-020f-41f3-aaf7-82976d62689a">
	<property name="ireport.zoom" value="1.0"/>
	<property name="ireport.x" value="0"/>
	<property name="ireport.y" value="0"/>
	<queryString>
		<![CDATA[SELECT
     factura."Id_factura" AS factura_Id_factura,
     factura."Fecha" AS factura_Fecha,
     factura."Cantidad_f" AS factura_Cantidad_f,
     factura."Total" AS factura_Total,
     factura."Id_ClientePK" AS factura_Id_ClientePK,
     factura."Id_ProductoPK" AS factura_Id_ProductoPK,
     Cliente."Id_cliente" AS Cliente_Id_cliente,
     Cliente."Nombres" AS Cliente_Nombres,
     Cliente."Apellido" AS Cliente_Apellido,
     producto."Id_Producto" AS producto_Id_Producto,
     producto."Nombre" AS producto_Nombre,
     producto."Precio_venta" AS producto_Precio_venta,
     producto."Id_Compra_ProductoPK" AS producto_Id_Compra_ProductoPK
FROM
     "dbo"."Cliente" Cliente INNER JOIN "dbo"."factura" factura ON Cliente."Id_cliente" = factura."Id_ClientePK"
     INNER JOIN "dbo"."producto" producto ON factura."Id_ProductoPK" = producto."Id_Producto"]]>
	</queryString>
	<field name="factura_Id_factura" class="java.lang.Integer"/>
	<field name="factura_Fecha" class="java.lang.String"/>
	<field name="factura_Cantidad_f" class="java.lang.Integer"/>
	<field name="factura_Total" class="java.math.BigDecimal"/>
	<field name="factura_Id_ClientePK" class="java.lang.Integer"/>
	<field name="factura_Id_ProductoPK" class="java.lang.Integer"/>
	<field name="Cliente_Id_cliente" class="java.lang.Integer"/>
	<field name="Cliente_Nombres" class="java.lang.String"/>
	<field name="Cliente_Apellido" class="java.lang.String"/>
	<field name="producto_Id_Producto" class="java.lang.Integer"/>
	<field name="producto_Nombre" class="java.lang.String"/>
	<field name="producto_Precio_venta" class="java.math.BigDecimal"/>
	<field name="producto_Id_Compra_ProductoPK" class="java.lang.Integer"/>
	<background>
		<band splitType="Stretch"/>
	</background>
	<title>
		<band height="79" splitType="Stretch"/>
	</title>
	<pageHeader>
		<band height="35" splitType="Stretch"/>
	</pageHeader>
	<columnHeader>
		<band height="31" splitType="Stretch">
			<staticText>
				<reportElement x="22" y="2" width="100" height="20" uuid="d71b4bc5-27d4-4c03-8d90-626a6caf207d"/>
				<text><![CDATA[factura_Id_factura]]></text>
			</staticText>
			<staticText>
				<reportElement x="159" y="2" width="100" height="20" uuid="f3f18d3b-3e38-49ce-963d-bc7c35ac9014"/>
				<text><![CDATA[producto_Nombre]]></text>
			</staticText>
			<staticText>
				<reportElement x="291" y="2" width="100" height="20" uuid="e3c18479-3e5e-4c9e-b8ed-75823cb8620c"/>
				<text><![CDATA[producto_Precio_venta]]></text>
			</staticText>
			<staticText>
				<reportElement x="436" y="2" width="100" height="20" uuid="e2b6f2c1-ad39-47c4-8301-78501256336a"/>
				<text><![CDATA[factura_Total]]></text>
			</staticText>
			<staticText>
				<reportElement x="599" y="2" width="100" height="20" uuid="bfed9b30-1732-4814-92a8-55f7497a3331"/>
				<text><![CDATA[Cliente_Nombres]]></text>
			</staticText>
		</band>
	</columnHeader>
	<detail>
		<band height="45" splitType="Stretch">
			<textField>
				<reportElement x="22" y="16" width="100" height="20" uuid="5f9af969-55e9-4924-b7a0-0cb0fb12fbd3"/>
				<textFieldExpression><![CDATA[$F{factura_Id_factura}]]></textFieldExpression>
			</textField>
			<textField>
				<reportElement x="159" y="20" width="100" height="20" uuid="115631bb-0d64-4ab3-92a3-050978a93275"/>
				<textFieldExpression><![CDATA[$F{producto_Nombre}]]></textFieldExpression>
			</textField>
			<textField>
				<reportElement x="291" y="20" width="100" height="20" uuid="9315097e-635c-479a-a610-436d71d7f2fd"/>
				<textFieldExpression><![CDATA[$F{producto_Precio_venta}]]></textFieldExpression>
			</textField>
			<textField>
				<reportElement x="436" y="18" width="100" height="20" uuid="b39b439f-f8a7-44be-ad28-19860f22f9cf"/>
				<textFieldExpression><![CDATA[$F{factura_Total}]]></textFieldExpression>
			</textField>
			<textField>
				<reportElement x="599" y="21" width="100" height="20" uuid="bfc20ac3-6af1-424c-8d1a-11c25feb4b9f"/>
				<textFieldExpression><![CDATA[$F{Cliente_Nombres}]]></textFieldExpression>
			</textField>
		</band>
	</detail>
	<columnFooter>
		<band height="20" splitType="Stretch"/>
	</columnFooter>
	<pageFooter>
		<band height="23" splitType="Stretch"/>
	</pageFooter>
	<summary>
		<band height="18" splitType="Stretch"/>
	</summary>
</jasperReport>
