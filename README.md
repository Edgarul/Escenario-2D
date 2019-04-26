# Escenario-2D
Escenarios terminados
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Esecnario2dPro
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void pictureBox1_Paint(object sender, PaintEventArgs e)
        {
            /*------------------------------------------------------ESCENARIO 1-----------------------------------------------------------------------------------------------*/

            /*----------------------------------------------ELEMENTOS NECESARIOS PARA DIBUJAR------------------------------------------------------------------*/
            Pen lapiz = new Pen(Color.Black, 1.75f);
            ColorDialog color = new ColorDialog();
            SolidBrush whiteBrush = new SolidBrush(Color.FromArgb(255, 255, 255));


            /*-------------------------------------------------------PUNTOS CON LAS COORDENADAS---------------------------------------------------------------------*/
            Point[] LateralIzq1 =
             {
                new Point(89, 322), new Point(138, 274), new Point(160, 274), new Point(176, 257), new Point(172, 233), new Point(182, 226),
                new Point(182, 218), new Point(190, 218), new Point(205, 201), new Point(214, 201), new Point(216, 178), new Point(224, 199),
                new Point(228, 199), new Point(223, 179), new Point(224, 157), new Point(222, 104), new Point(203, 99), new Point(174, 46),
                new Point(168, 38), new Point(0, 37), new Point(0, 318), new Point(86, 321),
            };

            Point[] Tabla =
          {
            new Point(229, 196), new Point(218, 164), new Point(214, 167), new Point(223, 199)
            };


            Point[] BarraIzquierda =
            {
            new Point(160, 273), new Point(178, 255), new Point(178, 90), new Point(160, 74), new Point(161, 272),
            };

            Point[] DerechaSombra =
            {
            new Point(176, 90), new Point(171, 39), new Point(81, 37), new Point(91, 318), new Point(138, 274), new Point(161, 274),
                new Point(160, 77),
            };

            Point[] PuertaDerecha =
            {
            new Point(189, 219), new Point(190, 135), new Point(181, 126), new Point(182, 220), new Point(181, 218),
            };

            Point[] LaterlDerecha1 =
             {
            new Point(394, 321), new Point(350, 276), new Point(326, 278), new Point(307, 256), new Point(310, 239), new Point(300, 227),
                new Point(302, 218), new Point(291, 218), new Point(274, 202), new Point(265, 201), new Point(262, 146), new Point(266, 139),
                new Point(275, 139), new Point(274, 96), new Point(310, 40), new Point(325, 38), new Point(352, 41), new Point(457, 39),
                new Point(456, 320), new Point(400, 320),
            };

            Point[] BarraDerecha =
            {
            new Point(324, 275), new Point(327, 75), new Point(312, 82), new Point(307, 257), new Point(323, 274),
            };

            Point[] BarraDerechaSombra =
           {
            new Point(326, 72), new Point(328, 39), new Point(310, 39), new Point(311, 86), new Point(327, 73),
            };

            Point[] PuertaIzquierda =
           {
            new Point(303, 229), new Point(304, 127), new Point(292, 132), new Point(291, 219), new Point(300, 216),
            };

            Point[] Fondo =
           {
                new Point(262, 190), new Point(256, 191), new Point(255, 152), new Point(226, 153), new Point(223, 174),
                new Point(231, 173), new Point(232, 161), new Point(243, 161), new Point(245, 171), new Point(253, 171),
                new Point(256, 191),

            };

            Point[] Marco =
            {
                new Point(216, 147), new Point(262, 149), new Point(264, 194), new Point(256, 194), new Point(255, 155), new Point(225, 156),
                new Point(222, 174), new Point(215, 163),
            };

            Point[] ContronoPuerta =
            {
               new Point(223, 173), new Point(233, 173), new Point(233, 185), new Point(245, 187), new Point(246, 172), new Point(253, 173), new Point(254, 187),
                new Point(228, 187),
            };

            Point[] Piso =
            {
            new Point(90, 322), new Point(137, 273), new Point(160, 276), new Point(177, 255), new Point(172, 236), new Point(182, 228),
                new Point(181, 217), new Point(189, 219), new Point(206, 202), new Point(214, 202), new Point(217, 182), new Point(223, 200), new Point(229, 194),
                new Point(226, 188), new Point(253, 188), new Point(255, 194), new Point(260, 193), new Point(264, 202), new Point(273, 204),
                new Point(290, 221), new Point(300, 218), new Point(300, 231), new Point(309, 237), new Point(308, 255), new Point(324, 279),
                new Point(345, 275), new Point(396, 322),

            };

            Point[] Puerta =
            {
              new Point(232, 185), new Point(245, 186), new Point(247, 160), new Point(234, 160),
            };


            Point[] Techo =
            {
            new Point(173, 40), new Point(313, 39), new Point(275, 89), new Point(277, 137), new Point(263, 140), new Point(262, 147),
                new Point(218, 148), new Point(218, 140), new Point(203, 136), new Point(203, 98),

            };

            Point[] ContronoTecho =
            {
            new Point(205, 203), new Point(205, 100), new Point(281, 100), new Point(276, 201), new Point(265, 203), new Point(263, 143), new Point(218, 148),
                new Point(218, 142), new Point(204, 141),

            };

            Point[] Lampara =
            {
            new Point(218, 128), new Point(221, 131), new Point(266, 113), new Point(263, 109), new Point(236, 119),

            };

            Point[] ColganteIzquierdo =
            {
            new Point(223, 123), new Point(226, 121), new Point(227, 58), new Point(223, 58),

            };


            Point[] ColganteDerecho =
            {
            new Point(252, 113), new Point(256, 111), new Point(255, 57), new Point(252, 57),

            };

            Point[] AzulejoVertical =
           {
            new Point(126, 323), new Point(213, 201), new Point(224, 201), new Point(166, 321), new Point(205, 322), new Point(234, 188),
                new Point(240, 188), new Point(239, 320), new Point(280, 320), new Point(245, 189), new Point(251, 189), new Point(319, 322),
                new Point(355, 320), new Point(264, 201), new Point(275, 202), new Point(310, 243), new Point(307, 257), new Point(323, 277),
                new Point(345, 276), new Point(394, 321),

            };

            Point[] AzulejoHorizontal =
          {
                new Point(109, 303), new Point(383, 309), new Point(364, 290), new Point(123, 289), new Point(136, 274), new Point(324, 278),
                new Point(315, 267), new Point(171, 265), new Point(176, 254), new Point(305, 258), new Point(308, 251), new Point(175, 249),
                new Point(174, 243), new Point(309, 245), new Point(308, 238), new Point(177, 235), new Point(180, 231), new Point(302, 231),
                new Point(299, 226), new Point(185, 226), new Point(190, 219), new Point(292, 223), new Point(287, 219), new Point(196, 213),
                new Point(202, 207), new Point(281, 210), new Point(278, 206), new Point(207, 203), new Point(213, 202), new Point(274, 205),
                new Point(266, 204), new Point(216, 200), new Point(226, 200), new Point(265, 199), new Point(262, 196), new Point(229, 193),


            };

            Point[] BarraIzquierda1 =
        {
            new Point(133, 274), new Point(160, 274), new Point(176, 257), new Point(179, 44), new Point(154, 40), new Point(107, 42),



            };

            Point[] Decoraciones1 =
        {
               new Point(178, 106), new Point(206, 135), new Point(275, 136), new Point(311, 104), new Point(311, 109), new Point(275, 138), new Point(205, 139), new Point(178, 112),
            };


            Point[] SombreadoIz =
        {
            new Point(324, 276), new Point(326, 70), new Point(312, 86), new Point(312, 39), new Point(413, 36), new Point(407, 320), new Point(395, 321), new Point(350, 276),
            };

            Point[] SombreadoDere =
        {
           new Point(176, 88), new Point(161, 75), new Point(162, 264), new Point(174, 253),
            };

            /*-----------------------------------------------------DIBUJAR LOS POLIGONOS Y RELLENO--------------------------------------------------------------*/

            whiteBrush = new SolidBrush(Color.FromArgb(210, 180, 140));
            e.Graphics.FillPolygon(whiteBrush, LateralIzq1);
            e.Graphics.DrawPolygon(lapiz, LateralIzq1);

            e.Graphics.FillPolygon(whiteBrush, LaterlDerecha1); ;
            e.Graphics.DrawPolygon(lapiz, LaterlDerecha1);

            whiteBrush = new SolidBrush(Color.FromArgb(245, 222, 179));

            e.Graphics.FillPolygon(whiteBrush, BarraDerecha);
            e.Graphics.DrawPolygon(lapiz, BarraDerecha);

            whiteBrush = new SolidBrush(Color.FromArgb(30, 50, 50));
            e.Graphics.FillPolygon(whiteBrush, BarraDerechaSombra);
            e.Graphics.DrawPolygon(lapiz, BarraDerechaSombra);


            whiteBrush = new SolidBrush(Color.FromArgb(222, 184, 135));
            e.Graphics.FillPolygon(whiteBrush, Tabla);
            e.Graphics.DrawPolygon(lapiz, Tabla);


            whiteBrush = new SolidBrush(Color.FromArgb(245, 222, 179));
            e.Graphics.FillPolygon(whiteBrush, BarraIzquierda);
            e.Graphics.DrawPolygon(lapiz, BarraIzquierda);

            whiteBrush = new SolidBrush(Color.FromArgb(30, 35, 35));
            e.Graphics.FillPolygon(whiteBrush, DerechaSombra);
            e.Graphics.DrawPolygon(lapiz, DerechaSombra);


            whiteBrush = new SolidBrush(Color.FromArgb(30, 50, 50));
            e.Graphics.FillPolygon(whiteBrush, PuertaDerecha);
            e.Graphics.DrawPolygon(lapiz, PuertaDerecha);


            whiteBrush = new SolidBrush(Color.FromArgb(30, 50, 50));
            e.Graphics.FillPolygon(whiteBrush, PuertaIzquierda);
            e.Graphics.DrawPolygon(lapiz, PuertaIzquierda);


            whiteBrush = new SolidBrush(Color.FromArgb(95, 60, 50));
            e.Graphics.FillPolygon(whiteBrush, Fondo);
            e.Graphics.DrawPolygon(lapiz, Fondo);


            whiteBrush = new SolidBrush(Color.FromArgb(120, 60, 50));
            e.Graphics.FillPolygon(whiteBrush, Marco);
            e.Graphics.DrawPolygon(lapiz, Marco);

            whiteBrush = new SolidBrush(Color.FromArgb(112, 128, 144));
            e.Graphics.FillPolygon(whiteBrush, Puerta);
            whiteBrush = new SolidBrush(Color.FromArgb(112, 128, 144));
            e.Graphics.DrawPolygon(lapiz, Puerta);
            whiteBrush = new SolidBrush(Color.FromArgb(60, 58, 44));
            e.Graphics.FillPolygon(whiteBrush, ContronoPuerta);
            e.Graphics.DrawPolygon(lapiz, ContronoPuerta);

            e.Graphics.FillPolygon(whiteBrush, Piso);
            e.Graphics.DrawPolygon(lapiz, Piso);

            whiteBrush = new SolidBrush(Color.FromArgb(60, 48, 34));
            e.Graphics.FillPolygon(whiteBrush, Techo);
            e.Graphics.DrawPolygon(lapiz, Techo);

            whiteBrush = new SolidBrush(Color.FromArgb(210, 180, 140));
            e.Graphics.FillPolygon(whiteBrush, ContronoTecho);
            e.Graphics.DrawPolygon(lapiz, ContronoTecho);

            whiteBrush = new SolidBrush(Color.FromArgb(255, 255, 205));
            e.Graphics.FillPolygon(whiteBrush, Lampara);
            e.Graphics.DrawPolygon(lapiz, Lampara);

            whiteBrush = new SolidBrush(Color.FromArgb(0, 0, 0));
            e.Graphics.FillPolygon(whiteBrush, ColganteIzquierdo);
            e.Graphics.DrawPolygon(lapiz, ColganteIzquierdo);
            e.Graphics.FillPolygon(whiteBrush, ColganteDerecho);
            e.Graphics.DrawPolygon(lapiz, ColganteDerecho);

            whiteBrush = new SolidBrush(Color.FromArgb(60, 48, 34));
            e.Graphics.FillPolygon(whiteBrush, AzulejoVertical);
            e.Graphics.DrawPolygon(lapiz, AzulejoVertical);
            whiteBrush = new SolidBrush(Color.FromArgb(50, 38, 34));
            e.Graphics.FillPolygon(whiteBrush, AzulejoHorizontal);
            e.Graphics.DrawPolygon(lapiz, AzulejoHorizontal);

            whiteBrush = new SolidBrush(Color.FromArgb(30, 35, 35));

            e.Graphics.FillPolygon(whiteBrush, BarraIzquierda1);
            e.Graphics.DrawPolygon(lapiz, BarraIzquierda1);

            whiteBrush = new SolidBrush(Color.FromArgb(60, 48, 34));
            e.Graphics.FillPolygon(whiteBrush, Decoraciones1);
            e.Graphics.DrawPolygon(lapiz, Decoraciones1);

            whiteBrush = new SolidBrush(Color.FromArgb(30, 35, 35));
            e.Graphics.DrawPolygon(lapiz, SombreadoIz);
            e.Graphics.FillPolygon(whiteBrush, SombreadoIz);

            whiteBrush = new SolidBrush(Color.FromArgb(245, 222, 179));
            e.Graphics.DrawPolygon(lapiz, SombreadoDere);
            e.Graphics.FillPolygon(whiteBrush, SombreadoDere);

            whiteBrush = new SolidBrush(Color.FromArgb(245, 222, 179));
            e.Graphics.DrawPolygon(lapiz, SombreadoDere);
            e.Graphics.FillPolygon(whiteBrush, SombreadoDere);



            lapiz = new Pen(Color.Black, 10);
            e.Graphics.DrawLine(lapiz, new Point(91, 321), new Point(81, 36));
            e.Graphics.DrawLine(lapiz, new Point(407, 318), new Point(411, 37));
        }




        private void pictureBox2_Paint(object sender, PaintEventArgs e)
        {
            /*------------------------------------------------------ESCENARIO 2-----------------------------------------------------------------------------------------------*/
            /*----------------------------------------------ELEMENTOS NECESARIOS PARA DIBUJAR------------------------------------------------------------------*/

            Pen lapiz = new Pen(Color.Black, 1.75f);
            ColorDialog color = new ColorDialog();
            SolidBrush whiteBrush = new SolidBrush(Color.FromArgb(255, 255, 255));


            /*-------------------------------------------------------PUNTOS CON LAS COORDENADAS---------------------------------------------------------------------*/

            Point[] LateralDere =
             {
            new Point(331, 351), new Point(255, 241), new Point(256, 227), new Point(229, 192), new Point(221, 192), new Point(157, 102),
                new Point(157, 31), new Point(177, 10), new Point(457, 9), new Point(457, 352), new Point(336, 352),
            };

            Point[] LateralIzq =
             {
              new Point(21, 348), new Point(55, 278), new Point(32, 217), new Point(73, 213), new Point(108, 102), new Point(93, 11),
                new Point(0, 8), new Point(0, 350),

            };

            Point[] Puerta =
             {

            new Point(229, 189), new Point(256, 226), new Point(263, 78), new Point(230, 72),

            };

            Point[] Chapa =
             {

            new Point(237, 159), new Point(232, 160), new Point(231, 134), new Point(238, 132), new Point(238, 136), new Point(235, 136), new Point(235, 156), new Point(237, 157),

            };

            Point[] Marco1 =
             {
            new Point(458, 336), new Point(257, 166), new Point(255, 240), new Point(332, 351), new Point(457, 353),

            };

            Point[] Marco2 =
             {
            new Point(230, 191), new Point(231, 133), new Point(221, 134), new Point(163, 87), new Point(163, 108), new Point(219, 192),

            };

            Point[] Marco3 =
             {
            new Point(17, 350), new Point(53, 279), new Point(27, 196), new Point(0, 230), new Point(1, 349),

            };

            Point[] Marco4 =
             {
            new Point(10, 149), new Point(58, 148), new Point(105, 83), new Point(109, 99), new Point(71, 213), new Point(32, 215),

            };

            Point[] VentanaP =
             {
            new Point(258, 151), new Point(242, 141), new Point(243, 86), new Point(260, 91),

            };


            Point[] Sombra =
             {
            new Point(165, 110), new Point(106, 112), new Point(92, 23), new Point(66, 11), new Point(190, 10),
                new Point(151, 38), new Point(161, 42), new Point(159, 97),

            };

            Point[] Piso =
             {
            new Point(105, 113), new Point(163, 105), new Point(218, 193), new Point(227, 192), new Point(256, 229), new Point(253, 238), new Point(328, 348), new Point(21, 350), new Point(52, 283), new Point(32, 221), new Point(74, 214),

            };

            Point[] Muerto1 =
            {
                new Point(48, 306), new Point(52, 306), new Point(56, 305), new Point(59, 303), new Point(60, 303),
                new Point(62, 303), new Point(67, 303), new Point(68, 303), new Point(73, 298), new Point(76, 298),
                new Point(82, 294), new Point(84, 291), new Point(87, 288), new Point(90, 284), new Point(92, 282),
                new Point(93, 280), new Point(98, 274), new Point(103, 273), new Point(104, 273), new Point(108, 273),
                new Point(109, 274), new Point(113, 276), new Point(117, 278), new Point(119, 279), new Point(121, 280),
                new Point(126, 280), new Point(127, 281), new Point(130, 281), new Point(135, 281), new Point(138, 281),
                new Point(142, 281), new Point(145, 280), new Point(147, 278), new Point(150, 275), new Point(151, 273),
                new Point(154, 269), new Point(156, 267), new Point(158, 264), new Point(160, 261), new Point(164, 256),
                new Point(166, 254), new Point(168, 252), new Point(174, 249), new Point(175, 249), new Point(178, 249),
                new Point(181, 248), new Point(182, 246), new Point(180, 245), new Point(175, 242), new Point(173, 242),
                new Point(170, 241), new Point(168, 241), new Point(164, 241), new Point(163, 242), new Point(160, 246),
                new Point(158, 249), new Point(156, 251), new Point(154, 254), new Point(152, 257), new Point(150, 259),
                new Point(148, 261), new Point(147, 264), new Point(144, 269), new Point(138, 269), new Point(135, 267),
                new Point(132, 266), new Point(128, 265), new Point(126, 264), new Point(121, 261), new Point(119, 260),
                new Point(117, 259), new Point(123, 255), new Point(127, 254), new Point(128, 254), new Point(132, 252),
                new Point(136, 250), new Point(139, 248), new Point(142, 247), new Point(147, 244), new Point(148, 244),
                new Point(151, 243), new Point(155, 240), new Point(159, 239), new Point(163, 238), new Point(165, 235),
                new Point(169, 230), new Point(171, 228), new Point(170, 227), new Point(167, 226), new Point(163, 226),
                new Point(160, 226), new Point(159, 226), new Point(153, 228), new Point(149, 232), new Point(149, 232),
                new Point(146, 234), new Point(139, 237), new Point(135, 238), new Point(132, 239), new Point(131, 240),
                new Point(128, 241), new Point(124, 242), new Point(120, 242), new Point(114, 243), new Point(111, 243),
                new Point(108, 244), new Point(105, 245), new Point(101, 247), new Point(97, 247), new Point(93, 250), new Point(91, 251),
                new Point(89, 253), new Point(85, 257), new Point(83, 258), new Point(81, 259), new Point(79, 260), new Point(71, 265),
                new Point(69, 266), new Point(66, 269), new Point(64, 270), new Point(63, 271), new Point(60, 274), new Point(59, 275),
                new Point(55, 279), new Point(55, 280), new Point(55, 280), new Point(55, 283), new Point(55, 284), new Point(55, 287),
                new Point(51, 288), new Point(47, 291), new Point(46, 291), new Point(43, 292), new Point(41, 295), new Point(40, 302),
                new Point(43, 303), new Point(46, 304), new Point(52, 304),
            };

            Point[] CharcoSangre1 =
           {
             new Point(44, 322), new Point(45, 324), new Point(47, 325), new Point(50, 327), new Point(52, 329), new Point(56, 329), new Point(59, 329), new Point(63, 329),
                new Point(66, 329), new Point(71, 327), new Point(77, 322), new Point(78, 321), new Point(81, 319), new Point(84, 318), new Point(84, 318), new Point(90, 318),
                new Point(93, 318), new Point(96, 315), new Point(97, 315), new Point(100, 315), new Point(105, 317), new Point(106, 317), new Point(109, 317), new Point(114, 317),
                new Point(116, 315), new Point(119, 312), new Point(122, 311), new Point(126, 310), new Point(129, 307), new Point(131, 305), new Point(138, 305), new Point(139, 304),
                new Point(144, 297), new Point(147, 296), new Point(150, 293), new Point(156, 290), new Point(161, 286), new Point(161, 285), new Point(161, 280), new Point(157, 275),
                new Point(156, 273), new Point(155, 270), new Point(151, 266), new Point(149, 264), new Point(147, 264), new Point(142, 263), new Point(139, 263), new Point(137, 263),
                new Point(133, 262), new Point(127, 260), new Point(126, 258), new Point(125, 253), new Point(120, 249), new Point(118, 246), new Point(112, 242), new Point(106, 242),
                new Point(102, 240), new Point(99, 240), new Point(96, 240), new Point(90, 241), new Point(87, 243), new Point(82, 246), new Point(80, 247), new Point(73, 247), new Point(64, 248),
                new Point(62, 252), new Point(60, 256), new Point(60, 259), new Point(60, 262), new Point(60, 264), new Point(58, 267), new Point(55, 270), new Point(53, 273), new Point(54, 276),
                new Point(55, 277), new Point(57, 279), new Point(58, 281), new Point(57, 284), new Point(53, 288), new Point(50, 292), new Point(48, 295), new Point(47, 298), new Point(46, 302),
                new Point(45, 303), new Point(43, 307), new Point(43, 313),

            };

            Point[] CharcoSangre2 =
           {
            new Point(125, 156), new Point(123, 155), new Point(121, 158), new Point(119, 162), new Point(119, 163), new Point(122, 164), new Point(125, 164), new Point(127, 164), new Point(134, 166),
                new Point(136, 168), new Point(137, 169), new Point(140, 169), new Point(143, 169), new Point(145, 169), new Point(149, 169), new Point(152, 169), new Point(156, 169),
                new Point(158, 169), new Point(164, 169), new Point(166, 169), new Point(172, 168), new Point(176, 167), new Point(178, 164), new Point(179, 161), new Point(179, 160),
                new Point(182, 156), new Point(184, 154), new Point(183, 152), new Point(180, 151), new Point(176, 149), new Point(174, 149), new Point(172, 149), new Point(165, 151),
                new Point(161, 151), new Point(157, 151), new Point(154, 151), new Point(149, 151), new Point(146, 151), new Point(140, 151), new Point(135, 153), new Point(131, 154),
                new Point(125, 155), new Point(125, 155),
            };

            Point[] Botas =
             {
            new Point(158, 262), new Point(152, 261), new Point(151, 259), new Point(154, 256), new Point(159, 252), new Point(159, 250), new Point(159, 247), new Point(163, 242),
                new Point(167, 240), new Point(170, 240), new Point(172, 240), new Point(174, 240), new Point(179, 241), new Point(181, 242), new Point(181, 245), new Point(181, 246),
                new Point(177, 248), new Point(172, 248), new Point(167, 252), new Point(165, 253), new Point(160, 257), new Point(158, 259),
            };

            Point[] Botas1 =
             {
            new Point(137, 238), new Point(139, 240), new Point(140, 242), new Point(142, 245), new Point(143, 245), new Point(151, 238), new Point(154, 236), new Point(157, 235),
                new Point(161, 234), new Point(165, 232), new Point(168, 231), new Point(169, 227), new Point(169, 225), new Point(166, 225), new Point(159, 225), new Point(155, 228),
                new Point(149, 233), new Point(143, 236), new Point(140, 237),

            };

            Point[] Cara =
             {
            new Point(42, 300), new Point(48, 300), new Point(50, 299), new Point(54, 298), new Point(56, 296), new Point(59, 296), new Point(59, 296), new Point(62, 296), new Point(62, 296),
                new Point(64, 299), new Point(65, 301), new Point(65, 302), new Point(62, 303), new Point(61, 304), new Point(58, 308), new Point(57, 308), new Point(53, 308), new Point(48, 308),
                new Point(46, 308), new Point(43, 303), new Point(43, 303),
            };


            Point[] Azulejo1 =
             {
            new Point(303, 310), new Point(296, 313), new Point(286, 316), new Point(276, 319), new Point(269, 321), new Point(263, 311), new Point(257, 302), new Point(254, 297),
                new Point(251, 291), new Point(239, 294), new Point(227, 298), new Point(214, 299), new Point(208, 290), new Point(205, 283), new Point(203, 278), new Point(201, 269),
                new Point(199, 263), new Point(195, 255), new Point(189, 254), new Point(180, 256), new Point(172, 257), new Point(162, 258), new Point(164, 268), new Point(166, 276),
                new Point(168, 282), new Point(157, 283), new Point(148, 284), new Point(140, 287), new Point(135, 287), new Point(127, 289), new Point(127, 294), new Point(127, 302),
                new Point(127, 310), new Point(129, 317), new Point(119, 321), new Point(106, 324), new Point(97, 326), new Point(89, 328), new Point(84, 328), new Point(84, 322), new Point(84, 315),
                new Point(84, 309), new Point(76, 305), new Point(67, 307), new Point(60, 307), new Point(56, 308), new Point(49, 309), new Point(38, 310),
                new Point(17, 350),new Point(54, 352), new Point(89, 352), new Point(103, 352), new Point(117, 352), new Point(125, 352), new Point(137, 351), new Point(164, 351), new Point(172, 351),
                new Point(182, 351), new Point(196, 351), new Point(207, 352), new Point(220, 353), new Point(233, 353), new Point(243, 353), new Point(254, 353), new Point(267, 353), new Point(278, 353),
                new Point(287, 353), new Point(293, 354), new Point(303, 354), new Point(314, 354), new Point(332, 353),

            };



            Point[] Azulejo2 =
            {
             new Point(212, 292), new Point(249, 289), new Point(248, 267), new Point(212, 266),


            };

            Point[] Azulejo3 =
            {
            new Point(199, 240), new Point(225, 248), new Point(241, 233), new Point(245, 231), new Point(236, 215), new Point(208, 221), new Point(210, 227),


            };

            Point[] Azulejo4 =
           {
            new Point(78, 193), new Point(88, 199), new Point(102, 196), new Point(103, 200), new Point(127, 195), new Point(127, 187), new Point(147, 183), new Point(151, 186),
                new Point(153, 194), new Point(176, 193), new Point(176, 182), new Point(172, 183), new Point(174, 182), new Point(171, 179), new Point(178, 178), new Point(178, 181),
                new Point(191, 183), new Point(203, 176), new Point(189, 172), new Point(196, 172), new Point(202, 171), new Point(160, 102), new Point(105, 110), new Point(94, 140),
            };



            /*-----------------------------------------------------DIBUJAR LOS POLIGONOS Y RELLENO--------------------------------------------------------------*/


            whiteBrush = new SolidBrush(Color.FromArgb(216, 194, 180));
            e.Graphics.FillPolygon(whiteBrush, LateralDere);
            e.Graphics.DrawPolygon(lapiz, LateralDere);
            e.Graphics.FillPolygon(whiteBrush, LateralIzq);
            e.Graphics.DrawPolygon(lapiz, LateralIzq);

            whiteBrush = new SolidBrush(Color.FromArgb(63, 76, 85));

            e.Graphics.FillPolygon(whiteBrush, Puerta);
            e.Graphics.DrawPolygon(lapiz, Puerta);

            whiteBrush = new SolidBrush(Color.FromArgb(113, 132, 139));
            e.Graphics.FillPolygon(whiteBrush, Marco1);
            e.Graphics.DrawPolygon(lapiz, Marco1);
            e.Graphics.FillPolygon(whiteBrush, Marco2);
            e.Graphics.DrawPolygon(lapiz, Marco2);
            e.Graphics.FillPolygon(whiteBrush, Marco3);
            e.Graphics.DrawPolygon(lapiz, Marco3);
            e.Graphics.FillPolygon(whiteBrush, Marco4);
            e.Graphics.DrawPolygon(lapiz, Marco4);
            e.Graphics.DrawLine(lapiz, new Point(49, 275), new Point(0, 113));

            whiteBrush = new SolidBrush(Color.FromArgb(-2373468));
            e.Graphics.FillPolygon(whiteBrush, VentanaP);
            e.Graphics.DrawPolygon(lapiz, VentanaP);

            whiteBrush = new SolidBrush(Color.FromArgb(-8355712));
            e.Graphics.FillPolygon(whiteBrush, Chapa);
            e.Graphics.DrawPolygon(lapiz, Chapa);
            e.Graphics.DrawLine(lapiz, new Point(221, 193), new Point(220, 69));
            e.Graphics.DrawLine(lapiz, new Point(220, 69), new Point(231, 73));

            whiteBrush = new SolidBrush(Color.FromArgb(-16777216));
            e.Graphics.FillPolygon(whiteBrush, Sombra);
            e.Graphics.DrawPolygon(lapiz, Sombra);

            whiteBrush = new SolidBrush(Color.FromArgb(235, 205, 177));
            e.Graphics.FillPolygon(whiteBrush, Piso);
            e.Graphics.DrawPolygon(lapiz, Piso);


            whiteBrush = new SolidBrush(Color.FromArgb(101, 129, 141));
            e.Graphics.FillPolygon(whiteBrush, Azulejo1);
            e.Graphics.DrawPolygon(lapiz, Azulejo1);
            e.Graphics.FillPolygon(whiteBrush, Azulejo2);
            e.Graphics.DrawPolygon(lapiz, Azulejo2);
            e.Graphics.FillPolygon(whiteBrush, Azulejo3);
            e.Graphics.DrawPolygon(lapiz, Azulejo3);
            e.Graphics.FillPolygon(whiteBrush, Azulejo4);
            e.Graphics.DrawPolygon(lapiz, Azulejo4);
            whiteBrush = new SolidBrush(Color.FromArgb(34, 0, 1));
            e.Graphics.FillPolygon(whiteBrush, CharcoSangre1);
            e.Graphics.DrawPolygon(lapiz, CharcoSangre1);
            e.Graphics.FillPolygon(whiteBrush, CharcoSangre2);
            e.Graphics.DrawPolygon(lapiz, CharcoSangre2);
            whiteBrush = new SolidBrush(Color.FromArgb(156, 137, 122));
            e.Graphics.FillPolygon(whiteBrush, Muerto1);
            e.Graphics.DrawPolygon(lapiz, Muerto1);
            whiteBrush = new SolidBrush(Color.Black);
            e.Graphics.FillPolygon(whiteBrush, Botas);
            e.Graphics.DrawPolygon(lapiz, Botas);
            e.Graphics.FillPolygon(whiteBrush, Botas1);
            e.Graphics.DrawPolygon(lapiz, Botas1);
            e.Graphics.FillPolygon(whiteBrush, Cara);
            e.Graphics.DrawPolygon(lapiz, Cara);


            e.Graphics.DrawLine(lapiz, new Point(304, 310), new Point(158, 350));
            e.Graphics.DrawLine(lapiz, new Point(212, 300), new Point(22, 341));
            e.Graphics.DrawLine(lapiz, new Point(213, 298), new Point(232, 354));
            e.Graphics.DrawLine(lapiz, new Point(269, 320), new Point(287, 353));
            e.Graphics.DrawLine(lapiz, new Point(167, 286), new Point(180, 350));
            e.Graphics.DrawLine(lapiz, new Point(168, 281), new Point(203, 275));
            e.Graphics.DrawLine(lapiz, new Point(129, 320), new Point(128, 351));
            e.Graphics.DrawLine(lapiz, new Point(83, 316), new Point(83, 352));
            e.Graphics.DrawLine(lapiz, new Point(184, 172), new Point(154, 103));
            e.Graphics.DrawLine(lapiz, new Point(170, 180), new Point(144, 104));
            e.Graphics.DrawLine(lapiz, new Point(148, 182), new Point(133, 105));
            e.Graphics.DrawLine(lapiz, new Point(126, 185), new Point(122, 105));
            e.Graphics.DrawLine(lapiz, new Point(106, 185), new Point(113, 105));
            e.Graphics.DrawLine(lapiz, new Point(199, 158), new Point(83, 175));
            e.Graphics.DrawLine(lapiz, new Point(190, 145), new Point(86, 162));
            e.Graphics.DrawLine(lapiz, new Point(180, 131), new Point(90, 147));
            e.Graphics.DrawLine(lapiz, new Point(79, 193), new Point(205, 170));
            lapiz = new Pen(Color.FromArgb(31, 31, 31));
            e.Graphics.DrawLine(lapiz, new Point(170, 122), new Point(96, 134));
            lapiz = new Pen(Color.FromArgb(65, 65, 65));
            e.Graphics.DrawLine(lapiz, new Point(168, 112), new Point(100, 124));
            lapiz = new Pen(Color.Black);
            e.Graphics.DrawLine(lapiz, new Point(241, 232), new Point(215, 224));
            e.Graphics.DrawLine(lapiz, new Point(210, 226), new Point(215, 224));


            //Flecha
            lapiz = new Pen(Color.FromArgb(143, 78, 72), 5);
            lapiz.StartCap = System.Drawing.Drawing2D.LineCap.ArrowAnchor;
            e.Graphics.DrawLine(lapiz, new Point(301, 179), new Point(355, 185));
            e.Graphics.DrawString("TO HELL", new Font("Chiller", 26), whiteBrush = new SolidBrush(Color.FromArgb(143, 78, 72)), new Point(290, 145));
        }


        private void button1_Click(object sender, EventArgs e)
        {
            pictureBox1.Visible = true;
            pictureBox2.Visible = false;
        }

        private void button4_Click(object sender, EventArgs e)
        {
            pictureBox2.Visible = true;
            pictureBox1.Visible = false;
        }

        private void button3_Click(object sender, EventArgs e)
        {
            using (SaveFileDialog dlgSave = new SaveFileDialog())
            {
                dlgSave.Title = "Save Image";
                dlgSave.Filter = "Bitmap Images (*..png)|*.png|All Files (*.*)|*.*";
                if (dlgSave.ShowDialog(this) == DialogResult.OK)

                    using (Bitmap bmp = new Bitmap(pictureBox2.Width, pictureBox2.Height))
                    {
                        pictureBox2.DrawToBitmap(bmp, new Rectangle(0, 0, bmp.Width, bmp.Height));
                        bmp.Save(dlgSave.FileName);
                    }
            }
        }

        private void button2_Click(object sender, EventArgs e)
        {
            using (SaveFileDialog dlgSave = new SaveFileDialog())
            {
                dlgSave.Title = "Save Image";
                dlgSave.Filter = "Bitmap Images (*.png)|*.png|All Files (*.*)|*.*";
                if (dlgSave.ShowDialog(this) == DialogResult.OK)

                    using (Bitmap bmp = new Bitmap(pictureBox1.Width, pictureBox1.Height))
                    {
                        pictureBox1.DrawToBitmap(bmp, new Rectangle(0, 0, bmp.Width, bmp.Height));
                        bmp.Save(dlgSave.FileName);
                    }
            }
        }
    }
}
